---
original_file_path: api-reference/peripherals/adc/adc_calibration.rst
---

# Analog to Digital Converter (ADC) Calibration Driver

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## Introduction

In {IDF_TARGET_NAME}, the analog-to-digital converter (ADC) compares the input analog voltage to the reference, and determines each bit of the output digital result. By design, the ADC reference voltage for {IDF_TARGET_NAME} is 1100 mV. However, the true reference voltage can range from 1000 mV to 1200 mV among different chips. This guide introduces the ADC calibration driver to minimize the effect of different reference voltages, and get more accurate output results.

## Functional Overview

The following sections of this document cover the typical steps to install and use the ADC calibration driver:

::: list
- `adc-calibration-scheme-creation`{.interpreted-text role="ref"} - covers how to create a calibration scheme handle and delete the calibration scheme handle.
- `adc-result-conversion`{.interpreted-text role="ref"} - covers how to convert ADC raw result to calibrated result.
- `adc-thread-safety`{.interpreted-text role="ref"} - lists which APIs are guaranteed to be thread-safe by the driver.

\- `Minimize Noise <adc-minimize-noise>`{.interpreted-text role="ref"} - describes a general way to minimize the noise. :esp32: - `adc-kconfig-options`{.interpreted-text role="ref"} - lists the supported Kconfig options that can be used to make a different effect on driver behavior.
:::

### Calibration Scheme Creation {#adc-calibration-scheme-creation}

The ADC calibration driver provides ADC calibration scheme(s). From the calibration driver\'s point of view, an ADC calibration scheme is created for an ADC calibration handle `adc_cali_handle_t`{.interpreted-text role="cpp:type"}.

`adc_cali_check_scheme`{.interpreted-text role="cpp:func"} can be used to know which calibration scheme is supported on the chip. If you already know the supported schemes, this step can be skipped. Just call the corresponding function to create the scheme handle.

If you use your custom ADC calibration schemes, you could either modify this function `adc_cali_check_scheme`{.interpreted-text role="cpp:func"}, or just skip this step and call your custom creation function.

::::: only
esp32 or esp32s2 or esp32c2

#### ADC Calibration Line Fitting Scheme

{IDF_TARGET_NAME} supports `ADC_CALI_SCHEME_VER_LINE_FITTING`{.interpreted-text role="c:macro"} scheme. To create this scheme, set up `adc_cali_line_fitting_config_t`{.interpreted-text role="cpp:type"} first.

- `adc_cali_line_fitting_config_t::unit_id`{.interpreted-text role="cpp:member"}, the ADC that your ADC raw results are from.
- `adc_cali_line_fitting_config_t::atten`{.interpreted-text role="cpp:member"}, ADC attenuation that your ADC raw results use.
- `adc_cali_line_fitting_config_t::bitwidth`{.interpreted-text role="cpp:member"}, bit width of ADC raw result.

::: only
esp32

There is also a configuration `adc_cali_line_fitting_config_t::default_vref`{.interpreted-text role="cpp:member"}. Normally this can be simply set to 0. Line Fitting scheme does not rely on this value. However, if the Line Fitting scheme required eFuse bits are not burned on your board, the driver will rely on this value to do the calibration.

You can use `adc_cali_scheme_line_fitting_check_efuse`{.interpreted-text role="cpp:func"} to check the eFuse bits. Normally the Line Fitting scheme eFuse value is `ADC_CALI_LINE_FITTING_EFUSE_VAL_EFUSE_TP`{.interpreted-text role="c:macro"} or `ADC_CALI_LINE_FITTING_EFUSE_VAL_EFUSE_VREF`{.interpreted-text role="c:macro"}. This means the Line Fitting scheme uses calibration parameters burned in the eFuse to do the calibration.

When the Line Fitting scheme eFuse value is `ADC_CALI_LINE_FITTING_EFUSE_VAL_DEFAULT_VREF`{.interpreted-text role="c:macro"}, you need to set the `esp_adc_cali_line_fitting_init::default_vref`{.interpreted-text role="cpp:member"}. Default vref is an estimate of the ADC reference voltage provided as a parameter during calibration.
:::

After setting up the configuration structure, call `adc_cali_create_scheme_line_fitting`{.interpreted-text role="cpp:func"} to create a Line Fitting calibration scheme handle.

::: only
esp32s2

This function may fail due to reasons such as `ESP_ERR_INVALID_ARG`{.interpreted-text role="c:macro"} or `ESP_ERR_NO_MEM`{.interpreted-text role="c:macro"}. Especially, when the function returns `ESP_ERR_NOT_SUPPORTED`{.interpreted-text role="c:macro"}, this means the calibration scheme required eFuse bits are not burned on your board.
:::

``` c
ESP_LOGI(TAG, "calibration scheme version is %s", "Line Fitting");
adc_cali_line_fitting_config_t cali_config = {
    .unit_id = unit,
    .atten = atten,
    .bitwidth = ADC_BITWIDTH_DEFAULT,
};
ESP_ERROR_CHECK(adc_cali_create_scheme_line_fitting(&cali_config, &handle));
```

When the ADC calibration is no longer used, please delete the calibration scheme handle by calling `adc_cali_delete_scheme_line_fitting`{.interpreted-text role="cpp:func"}.

##### Delete Line Fitting Scheme

``` c
ESP_LOGI(TAG, "delete %s calibration scheme", "Line Fitting");
ESP_ERROR_CHECK(adc_cali_delete_scheme_line_fitting(handle));
```
:::::

::::: only
esp32c3 or esp32s3 or esp32c6 or esp32h2 or esp32c5 or esp32p4

#### ADC Calibration Curve Fitting Scheme

{IDF_TARGET_NAME} supports `ADC_CALI_SCHEME_VER_CURVE_FITTING`{.interpreted-text role="c:macro"} scheme. To create this scheme, set up `adc_cali_curve_fitting_config_t`{.interpreted-text role="cpp:type"} first.

::: only
esp32c3 or esp32s3

- `adc_cali_curve_fitting_config_t::unit_id`{.interpreted-text role="cpp:member"}, the ADC that your ADC raw results are from.
- `adc_cali_curve_fitting_config_t::chan`{.interpreted-text role="cpp:member"}, this member is kept here for extensibility. The calibration scheme only differs by attenuation, there is no difference among different channels.
- `adc_cali_curve_fitting_config_t::atten`{.interpreted-text role="cpp:member"}, ADC attenuation that your ADC raw results use.
- `adc_cali_curve_fitting_config_t::bitwidth`{.interpreted-text role="cpp:member"}, bit width of ADC raw result.
:::

::: only
esp32c6 or esp32h2 or esp32c5 or esp32p4

- `adc_cali_curve_fitting_config_t::unit_id`{.interpreted-text role="cpp:member"}, the ADC that your ADC raw results are from.
- `adc_cali_curve_fitting_config_t::chan`{.interpreted-text role="cpp:member"}, the ADC channel that your ADC raw results are from. The calibration scheme not only differs by attenuation but is also related to the channels.
- `adc_cali_curve_fitting_config_t::atten`{.interpreted-text role="cpp:member"}, ADC attenuation that your ADC raw results use.
- `adc_cali_curve_fitting_config_t::bitwidth`{.interpreted-text role="cpp:member"}, bit width of ADC raw result.
:::

After setting up the configuration structure, call `adc_cali_create_scheme_curve_fitting`{.interpreted-text role="cpp:func"} to create a Curve Fitting calibration scheme handle. This function may fail due to reasons such as `ESP_ERR_INVALID_ARG`{.interpreted-text role="c:macro"} or `ESP_ERR_NO_MEM`{.interpreted-text role="c:macro"}.

##### ADC Calibration eFuse Related Failures

When the function `adc_cali_create_scheme_curve_fitting`{.interpreted-text role="cpp:func"} returns `ESP_ERR_NOT_SUPPORTED`{.interpreted-text role="c:macro"}, this means the calibration scheme required eFuse bits are not correct on your board.

The ADC calibration scheme provided by ESP-IDF is based on the values in certain ADC calibration related on-chip eFuse bits. Espressif guarantees that these bits are burned during module manufacturing, so you don\'t have to burn these eFuses bits yourself.

If you see such an error, please contact us at [Technical Inquiries](https://www.espressif.com/en/contact-us/technical-inquiries) website.

##### Create Curve Fitting Scheme

``` c
ESP_LOGI(TAG, "calibration scheme version is %s", "Curve Fitting");
adc_cali_curve_fitting_config_t cali_config = {
    .unit_id = unit,
    .atten = atten,
    .bitwidth = ADC_BITWIDTH_DEFAULT,
};
ESP_ERROR_CHECK(adc_cali_create_scheme_curve_fitting(&cali_config, &handle));
```

When the ADC calibration is no longer used, please delete the calibration scheme driver from the calibration handle by calling `adc_cali_delete_scheme_curve_fitting`{.interpreted-text role="cpp:func"}.

##### Delete Curve Fitting Scheme

``` c
ESP_LOGI(TAG, "delete %s calibration scheme", "Curve Fitting");
ESP_ERROR_CHECK(adc_cali_delete_scheme_curve_fitting(handle));
```
:::::

:::: note
::: title
Note
:::

If you want to use your custom calibration schemes, you could provide a creation function to create your calibration scheme handle. Check the function table `adc_cali_scheme_t` in `components/esp_adc/interface/adc_cali_interface.h` to know the ESP ADC calibration interface.
::::

### Result Conversion {#adc-result-conversion}

After setting up the calibration characteristics, you can call `adc_cali_raw_to_voltage`{.interpreted-text role="cpp:func"} to convert the ADC raw result into calibrated result. The calibrated result is in the unit of mV. This function may fail due to an invalid argument. Especially, if this function returns `ESP_ERR_INVALID_STATE`{.interpreted-text role="c:macro"}, this means the calibration scheme is not created. You need to create a calibration scheme handle, use `adc_cali_check_scheme`{.interpreted-text role="cpp:func"} to know the supported calibration scheme. On the other hand, you could also provide a custom calibration scheme and create the handle.

::::: only
esp32c2

:::: note
::: title
Note
:::

ADC calibration is only supported under `ADC_ATTEN_DB_0`{.interpreted-text role="c:macro"} and `ADC_ATTEN_DB_12`{.interpreted-text role="c:macro"}. Under `ADC_ATTEN_DB_0`{.interpreted-text role="c:macro"}, the attenuation of ADC is set to 0 dB, and input voltage higher than 950 mV is not supported. Under `ADC_ATTEN_DB_12`{.interpreted-text role="c:macro"}, the attenuation of ADC is set to 11 dB, and input voltage higher than 2800 mV is not supported.
::::
:::::

##### Get Voltage

``` c
ESP_ERROR_CHECK(adc_cali_raw_to_voltage(adc_cali_handle, adc_raw[0][0], &voltage[0][0]));
ESP_LOGI(TAG, "ADC%d Channel[%d] Cali Voltage: %d mV", ADC_UNIT_1 + 1, EXAMPLE_ADC1_CHAN0, voltage[0][0]);
```

### Thread Safety {#adc-thread-safety}

The factory function `esp_adc_cali_new_scheme`{.interpreted-text role="cpp:func"} is guaranteed to be thread-safe by the driver. Therefore, you can call them from different RTOS tasks without protection by extra locks.

Other functions that take the `adc_cali_handle_t`{.interpreted-text role="cpp:type"} as the first positional parameter are not thread-safe, you should avoid calling them from multiple tasks.

::: only
esp32

### Kconfig Options {#adc-kconfig-options}

- `CONFIG_ADC_CALI_EFUSE_TP_ENABLE`{.interpreted-text role="ref"} - disable this to decrease the code size, if the calibration eFuse value is not set to `ADC_CALI_LINE_FITTING_EFUSE_VAL_EFUSE_TP`{.interpreted-text role="cpp:type"}.
- `CONFIG_ADC_CALI_EFUSE_VREF_ENABLE`{.interpreted-text role="ref"} - disable this to decrease the code size, if the calibration eFuse value is not set to `ADC_CALI_LINE_FITTING_EFUSE_VAL_EFUSE_VREF`{.interpreted-text role="cpp:type"}.
- `CONFIG_ADC_CALI_LUT_ENABLE`{.interpreted-text role="ref"} - disable this to decrease the code size, if you do not calibrate the ADC raw results under `ADC_ATTEN_DB_12`{.interpreted-text role="c:macro"}.
:::

### Minimize Noise {#adc-minimize-noise}

The {IDF_TARGET_NAME} ADC is sensitive to noise, leading to large discrepancies in ADC readings. Depending on the usage scenario, you may need to connect a bypass capacitor (e.g., a 100 nF ceramic capacitor) to the ADC input pad in use, to minimize noise. Besides, multisampling may also be used to further mitigate the effects of noise.

::: only
esp32

<figure class="align-center">
<img src="../../../../_static/diagrams/adc/adc-noise-graph.jpg" alt="ADC noise mitigation" />
<figcaption>Graph illustrating noise mitigation using capacitor and multisampling of 64 samples.</figcaption>
</figure>
:::

## API Reference

::: include-build-file
inc/adc_cali.inc
:::

::: include-build-file
inc/adc_cali_scheme.inc
:::
