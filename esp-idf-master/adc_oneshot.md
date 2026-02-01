---
original_file_path: api-reference/peripherals/adc/adc_oneshot.rst
---

# Analog to Digital Converter (ADC) Oneshot Mode Driver

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## Introduction

This document describes the ADC oneshot mode driver on {IDF_TARGET_NAME}.

Oneshot mode allows you to perform single, on-demand ADC conversions on selected analog input channels. It is suitable for applications that require infrequent or triggered sampling, as opposed to continuous data acquisition.

::: only
SOC_ADC_DMA_SUPPORTED

To perform continuous data acquisition, {IDF_TARGET_NAME} provides `ADC Continuous Mode Driver <adc_continuous>`{.interpreted-text role="doc"}.
:::

## Functional Overview

The following sections of this document cover the typical steps to install and operate an ADC:

- `adc-oneshot-resource-allocation`{.interpreted-text role="ref"} - covers which parameters should be set up to get an ADC handle and how to recycle the resources when ADC finishes working.
- `adc-oneshot-unit-configuration`{.interpreted-text role="ref"} - covers the parameters that should be set up to configure the ADC unit, so as to get ADC conversion raw result.
- `adc-oneshot-read-conversion-result`{.interpreted-text role="ref"} - covers how to get ADC conversion raw result.
- `hardware_limitations_adc_oneshot`{.interpreted-text role="ref"} - describes the ADC-related hardware limitations.
- `adc-oneshot-power-management`{.interpreted-text role="ref"} - covers power management-related information.
- `adc-oneshot-iram-safe`{.interpreted-text role="ref"} - describes tips on how to read ADC conversion raw results when the cache is disabled.
- `adc-oneshot-thread-safety`{.interpreted-text role="ref"} - lists which APIs are guaranteed to be thread-safe by the driver.
- `adc-oneshot-kconfig-options`{.interpreted-text role="ref"} - lists the supported Kconfig options that can be used to make a different effect on driver behavior.

### Resource Allocation {#adc-oneshot-resource-allocation}

The ADC oneshot mode driver is implemented based on {IDF_TARGET_NAME} SAR ADC module. Different ESP chips might have different numbers of independent ADCs. From the oneshot mode driver\'s point of view, an ADC instance is represented by `adc_oneshot_unit_handle_t`{.interpreted-text role="cpp:type"}.

To install an ADC instance, set up the required initial configuration structure `adc_oneshot_unit_init_cfg_t`{.interpreted-text role="cpp:type"}:

- `adc_oneshot_unit_init_cfg_t::unit_id`{.interpreted-text role="cpp:member"} selects the ADC. Please refer to the [datasheet]({IDF_TARGET_TRM_EN_URL}) to know dedicated analog IOs for this ADC.
- `adc_oneshot_unit_init_cfg_t::clk_src`{.interpreted-text role="cpp:member"} selects the source clock of the ADC. If set to 0, the driver will fall back to using a default clock source, see `adc_oneshot_clk_src_t`{.interpreted-text role="cpp:type"} to know the details.
- `adc_oneshot_unit_init_cfg_t::ulp_mode`{.interpreted-text role="cpp:member"} sets if the ADC will be working under ULP mode.

::: todo
Add ULP ADC-related docs here.
:::

After setting up the initial configurations for the ADC, call `adc_oneshot_new_unit`{.interpreted-text role="cpp:func"} with the prepared `adc_oneshot_unit_init_cfg_t`{.interpreted-text role="cpp:type"}. This function will return an ADC unit handle if the allocation is successful.

This function may fail due to various errors such as invalid arguments, insufficient memory, etc. Specifically, when the to-be-allocated ADC instance is registered already, this function will return `ESP_ERR_NOT_FOUND`{.interpreted-text role="c:macro"} error. Number of available ADC(s) is recorded by `SOC_ADC_PERIPH_NUM`{.interpreted-text role="c:macro"}.

If a previously created ADC instance is no longer required, you should recycle the ADC instance by calling `adc_oneshot_del_unit`{.interpreted-text role="cpp:func"}, related hardware and software resources will be recycled as well.

#### Create an ADC Unit Handle Under Normal Oneshot Mode

``` c
adc_oneshot_unit_handle_t adc1_handle;
adc_oneshot_unit_init_cfg_t init_config1 = {
    .unit_id = ADC_UNIT_1,
    .ulp_mode = ADC_ULP_MODE_DISABLE,
};
ESP_ERROR_CHECK(adc_oneshot_new_unit(&init_config1, &adc1_handle));
```

#### Recycle the ADC Unit

``` c
ESP_ERROR_CHECK(adc_oneshot_del_unit(adc1_handle));
```

### Unit Configuration {#adc-oneshot-unit-configuration}

After an ADC instance is created, set up the `adc_oneshot_chan_cfg_t`{.interpreted-text role="cpp:type"} to configure ADC IOs to measure analog signal:

- `adc_oneshot_chan_cfg_t::atten`{.interpreted-text role="cpp:member"}, ADC attenuation. Refer to [Datasheet]({IDF_TARGET_DATASHEET_EN_URL}) \> `ADC Characteristics`.
- `adc_oneshot_chan_cfg_t::bitwidth`{.interpreted-text role="cpp:member"}, the bitwidth of the raw conversion result.

:::: note
::: title
Note
:::

For the IO corresponding ADC channel number, check [datasheet]({IDF_TARGET_TRM_EN_URL}) to know the ADC IOs.

Additionally, `adc_continuous_io_to_channel`{.interpreted-text role="cpp:func"} and `adc_continuous_channel_to_io`{.interpreted-text role="cpp:func"} can be used to know the ADC channels and ADC IOs.
::::

To make these settings take effect, call `adc_oneshot_config_channel`{.interpreted-text role="cpp:func"} with the above configuration structure. You should specify an ADC channel to be configured as well. Function `adc_oneshot_config_channel`{.interpreted-text role="cpp:func"} can be called multiple times to configure different ADC channels. The Driver will save each of these channel configurations internally.

#### Configure Two ADC Channels

``` c
adc_oneshot_chan_cfg_t config = {
    .bitwidth = ADC_BITWIDTH_DEFAULT,
    .atten = ADC_ATTEN_DB_12,
};
ESP_ERROR_CHECK(adc_oneshot_config_channel(adc1_handle, EXAMPLE_ADC1_CHAN0, &config));
ESP_ERROR_CHECK(adc_oneshot_config_channel(adc1_handle, EXAMPLE_ADC1_CHAN1, &config));
```

### Read Conversion Result {#adc-oneshot-read-conversion-result}

After above configurations, the ADC is ready to measure the analog signal(s) from the configured ADC channel(s). Call `adc_oneshot_read`{.interpreted-text role="cpp:func"} to get the conversion raw result of an ADC channel.

- `adc_oneshot_read`{.interpreted-text role="cpp:func"} is safe to use. ADC(s) are shared by some other drivers/peripherals, see `hardware_limitations_adc_oneshot`{.interpreted-text role="ref"}. This function uses mutexes to avoid concurrent hardware usage. Therefore, this function should not be used in an ISR context. This function may fail when the ADC is in use by other drivers/peripherals, and return `ESP_ERR_TIMEOUT`{.interpreted-text role="c:macro"}. Under this condition, the ADC raw result is invalid.

This function will fail due to invalid arguments.

The ADC conversion results read from this function are raw data. To calculate the voltage based on the ADC raw results, this formula can be used:

::: parsed-literal
Vout = Dout \* Vmax / Dmax (1)
:::

where:

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Vout           Digital output result, standing for the voltage.
  -------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Dout           ADC raw digital reading result.

  Vmax           Maximum measurable input analog voltage, this is related to the ADC attenuation, please refer to [TRM]({IDF_TARGET_TRM_EN_URL}) \> `On-Chip Sensor and Analog Signal Processing`.

  Dmax           Maximum of the output ADC raw digital reading result, which is 2\^bitwidth, where bitwidth is the `adc_oneshot_chan_cfg_t::bitwidth`{.interpreted-text role="cpp:member"} configured before.
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

To do further calibration to convert the ADC raw result to voltage in mV, please refer to calibration doc `adc_calibration`{.interpreted-text role="doc"}.

#### Read Raw Result

``` c
ESP_ERROR_CHECK(adc_oneshot_read(adc1_handle, EXAMPLE_ADC1_CHAN0, &adc_raw[0][0]));
ESP_LOGI(TAG, "ADC%d Channel[%d] Raw Data: %d", ADC_UNIT_1 + 1, EXAMPLE_ADC1_CHAN0, adc_raw[0][0]);

ESP_ERROR_CHECK(adc_oneshot_read(adc1_handle, EXAMPLE_ADC1_CHAN1, &adc_raw[0][1]));
ESP_LOGI(TAG, "ADC%d Channel[%d] Raw Data: %d", ADC_UNIT_1 + 1, EXAMPLE_ADC1_CHAN1, adc_raw[0][1]);
```

### Hardware Limitations {#hardware_limitations_adc_oneshot}

::: list
\- Random Number Generator (RNG) uses ADC as an input source. When ADC `adc_oneshot_read`{.interpreted-text role="cpp:func"} works, the random number generated from RNG will be less random. :SOC_ADC_DMA_SUPPORTED: - A specific ADC unit can only work under one operating mode at any one time, either continuous mode or oneshot mode. `adc_oneshot_read`{.interpreted-text role="cpp:func"} has provided the protection. :esp32 or esp32s2 or esp32s3: - ADC2 is also used by Wi-Fi. `adc_oneshot_read`{.interpreted-text role="cpp:func"} has provided protection between the Wi-Fi driver and ADC oneshot mode driver. :esp32c3: - ADC2 oneshot mode is no longer supported, due to hardware limitations. The results are not stable. This issue can be found in [ESP32-C3 Series SoC Errata](https://www.espressif.com/sites/default/files/documentation/esp32-c3_errata_en.pdf). For compatibility, you can enable `CONFIG_ADC_ONESHOT_FORCE_USE_ADC2_ON_C3`{.interpreted-text role="ref"} to force use ADC2. :esp32: - ESP32-DevKitC: GPIO0 cannot be used in oneshot mode, because the DevKit has used it for auto-flash. :esp32: - ESP-WROVER-KIT: GPIO 0, 2, 4, and 15 cannot be used due to external connections for different purposes.
:::

### Power Management {#adc-oneshot-power-management}

When power management is enabled, i.e., `CONFIG_PM_ENABLE`{.interpreted-text role="ref"} is on, the system clock frequency may be adjusted when the system is in an idle state. However, the ADC oneshot mode driver works in a polling routine, the `adc_oneshot_read`{.interpreted-text role="cpp:func"} will poll the CPU until the function returns. During this period of time, the task in which ADC oneshot mode driver resides will not be blocked. Therefore the clock frequency is stable when reading.

### IRAM Safe {#adc-oneshot-iram-safe}

By default, all the ADC oneshot mode driver APIs are not supposed to be run when the Cache is disabled. Cache may be disabled due to many reasons, such as Flash writing/erasing, OTA, etc. If these APIs execute when the Cache is disabled, you will probably see errors like `Illegal Instruction` or `Load/Store Prohibited`.

### Thread Safety {#adc-oneshot-thread-safety}

- `adc_oneshot_new_unit`{.interpreted-text role="cpp:func"}
- `adc_oneshot_config_channel`{.interpreted-text role="cpp:func"}
- `adc_oneshot_read`{.interpreted-text role="cpp:func"}
- `adc_oneshot_del_unit`{.interpreted-text role="cpp:func"}

Above functions are guaranteed to be thread-safe. Therefore, you can call them from different RTOS tasks without protection by extra locks.

### Kconfig Options {#adc-oneshot-kconfig-options}

- `CONFIG_ADC_ONESHOT_CTRL_FUNC_IN_IRAM`{.interpreted-text role="ref"} controls where to place the ADC fast read function (IRAM or Flash), see [IRAM Safe](#iram-safe) for more details.

## Application Examples

- `peripherals/adc/oneshot_read`{.interpreted-text role="example"} demonstrates how to obtain a one-shot ADC reading from a GPIO pin using the ADC one-shot mode driver and how to use the ADC Calibration functions to obtain a calibrated result in mV on {IDF_TARGET_NAME}.

## API Reference

::: include-build-file
inc/adc_oneshot.inc
:::
