---
original_file_path: api-reference/peripherals/cap_touch_sens.rst
---

# Capacitive Touch Sensor

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

{IDF_TARGET_TOUCH_SENSOR_VERSION:default=\"NOT_UPDATED\", esp32=\"v1\", esp32s2=\"v2\", esp32s3=\"v2\", esp32p4=\"v3\", esp32h4=\"v3\"}

## Introduction

A touch sensor system is built on a substrate which carries electrodes and relevant connections under a protective flat surface. When the surface is touched, the capacitance variation is used to evaluate if the touch was valid.

The sensing pads can be arranged in different combinations (e.g., matrix, slider), so that a larger area or more points can be detected. The touch pad sensing process is under the control of a hardware-implemented finite-state machine (FSM) which is initiated by software or a dedicated hardware timer.

For design, operation, and control registers of a touch sensor, see **{IDF_TARGET_NAME} Technical Reference Manual** \> **On-Chip Sensors and Analog Signal Processing** \[[PDF]({IDF_TARGET_TRM_EN_URL}#sensor)\].

In-depth design details of touch sensors and firmware development guidelines for the {IDF_TARGET_NAME} are available in [Touch Sensor Application Note](https://github.com/espressif/esp-iot-solution/blob/release/v1.0/documents/touch_pad_solution/touch_sensor_design_en.md).

## Overview of Capacitive Touch Sensor Versions

+------------------+-------------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| Hardware Version | Chip              | Main Features                                                                                                                                  |
+==================+===================+================================================================================================================================================+
| V1               | ESP32             | Version 1, the channel value decreases when it is touched                                                                                      |
+------------------+-------------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| V2               | ESP32-S2          | Version 2, the channel value increases when it is touched Supports hardware filter, benchmark, waterproof, proximity sensing and sleep wake-up |
|                  +-------------------+------------------------------------------------------------------------------------------------------------------------------------------------+
|                  | ESP32-S3          | Version 2, support proximity measurement done interrupt                                                                                        |
+------------------+-------------------+------------------------------------------------------------------------------------------------------------------------------------------------+
| V3               | ESP32-P4 ESP32-H4 | Version 3, support frequency hopping                                                                                                           |
+------------------+-------------------+------------------------------------------------------------------------------------------------------------------------------------------------+

## Measurement Principle

The touch sensor will charge and discharge the touch channel by the internal current or voltage bias. Due to the internal capacitance and the stray capacitance in the circuit, the signals on the touch pins will present as a sawtooth wave. When the finger is approaching or touched on the touch pad, the capacitance of the touch channel increases, which leads to a slower charge and discharge, and a longer sawtooth period.

::: only
esp32

The touch sensor charges and discharges the touch channel within a fixed time and counts the number of charge-discharge cycles, and the count result serves as the raw data. The duration of a single charge-discharge measurement can be specified by `touch_sensor_sample_config_t::charge_times`{.interpreted-text role="cpp:member"}, and the interval between two measurements can be specified by `touch_sensor_config_t::meas_interval_us`{.interpreted-text role="cpp:member"}.

<figure class="align-center">
<img src="../../../_static/touch_pad-measurement-parameters.jpg" alt="Touch Pad - relationship between measurement parameters" />
<figcaption>Touch Sensor Working Principle</figcaption>
</figure>
:::

::: only
not esp32

The touch sensor counts the number of clock cycles spent for a fixed number of charge-discharge cycles, and the count result serves as the raw data. The number of charge-discharge cycles for a single measurement can be specified by `touch_sensor_sample_config_t::charge_duration_ms`{.interpreted-text role="cpp:member"}, and the interval between two measurements can be specified by `touch_sensor_config_t::meas_interval_us`{.interpreted-text role="cpp:member"}.

<figure class="align-center">
<img src="../../../_static/touch_pad-measurement-parameters-version2.png" alt="Touch Pad - relationship between measurement parameters" />
<figcaption>Touch Sensor Working Principle</figcaption>
</figure>
:::

## Overview of Touch Sensor Channels

## Terminology in the Driver

- **Touch Sensor Controller**: The controller of the touch sensor, responsible for configuring and managing the touch sensor.
- **Touch Sensor Channel**: A specific touch sensor sampling channel. A touch sensor module has multiple touch channels, which are usually connected to the touch pad for measuring the capacitance change. In the driver, sampling of **one** channel is called one `measurement` and the scanning of **all** registered channels is called one `scan`.

::: only
not esp32 and not esp32s2 and not esp32s3

- **Touch Sensor Sampling Configuration**: Touch sensor sampling configuration refers to all the hardware configurations that related to the sampling. It can determine how the touch channels sample by setting the number of charging times, charging frequency, measurement interval, etc. The {IDF_TARGET_NAME} supports multiple sets of sample configuration, which means it can support frequency hopping.
:::

::: only
esp32 or esp32s2 or esp32s3

- **Touch Sensor Sampling Configuration**: Touch sensor sampling configuration refers to all the hardware configurations that related to the sampling. It can determine how the touch channels sample by setting the number of charging times, charging frequency, measurement interval, etc. The {IDF_TARGET_NAME} only support one set of sample configuration, so it doesn\'t support frequency hopping.
:::

## File Structure

<figure class="align-center">
<img src="../../../_static/diagrams/cap_touch_sens/touch_file_structure.svg" alt="File Structure of Touch Sensor Driver" />
<figcaption aria-hidden="true">File Structure of Touch Sensor Driver</figcaption>
</figure>

## Finite-state Machine

The following diagram shows the state machine of the touch sensor driver, which describes the driver state after calling a function, and the constraint of the state transition.

<figure class="align-center">
<img src="../../../_static/diagrams/cap_touch_sens/touch_state_machine.svg" alt="Finite-state Machine of Touch Sensor Driver" />
<figcaption aria-hidden="true">Finite-state Machine of Touch Sensor Driver</figcaption>
</figure>

The diagram above is the finite-state machine of the touch sensor driver, which describes how the state transferred by invoking different APIs. `<other_configurations>` in the diagram stands for the other optional configurations, like reconfigurations to the touch sensor controller or channels, callback registration, filter, and so on.

:::: note
::: title
Note
:::

`touch_channel_read_data`{.interpreted-text role="cpp:func"} can be called at any time after the channel is registered (i.e., since `INIT` state), but please take care of the validation of the data.
::::

## Functionality Introduction

Categorized by functionality, the APIs of Capacitive Touch Sensor mainly include:

::: list
- [Touch Sensor Controller Management](#touch-ctrl)
- [Touch Sensor Channel Management](#touch-chan)
- [Filter Configuration](#touch-filter)
- [Callback](#touch-callback)
- [Enable and Disable](#touch-enable)
- [Continuous Scan](#touch-conti-scan)
- [Oneshot Scan](#touch-oneshot-scan)

\- [Read Measurement Data](#touch-read) :SOC_TOUCH_SUPPORT_BENCHMARK: - [Benchmark Configuration](#touch-benchmark) :SOC_TOUCH_SUPPORT_WATERPROOF: - [Waterproof Configuration](#touch-waterproof) :SOC_TOUCH_SUPPORT_PROX_SENSING: - [Proximity Sensing Configuration](#touch-prox-sensing) :SOC_TOUCH_SUPPORT_SLEEP_WAKEUP: - [Sleep Wake-up Configuration](#touch-sleep-wakeup) :SOC_TOUCH_SUPPORT_DENOISE_CHAN: - [Denoise Channel Configuration](#touch-denoise-chan)
:::

### Touch Sensor Controller Management {#touch-ctrl}

Touch Sensor is controlled by controller handle `touch_sensor_handle_t`{.interpreted-text role="cpp:type"}, it can be initialized and allocated by `touch_sensor_new_controller`{.interpreted-text role="cpp:func"}.

``` c
// Some target has multiple sets of sample configuration can be set, here take one for example
#define SAMPLE_NUM 1
touch_sensor_handle_t sens_handle = NULL;
// sample configuration
touch_sensor_sample_config_t sample_cfg[SAMPLE_NUM] = {
    // Specify sample configuration or apply the default sample configuration via `TOUCH_SENSOR_Vn_DEFAULT_SAMPLE_CONFIG`
    // ...
};
// Use the default touch controller configuration
touch_sensor_config_t touch_cfg = TOUCH_SENSOR_DEFAULT_BASIC_CONFIG(SAMPLE_NUM, sample_cfg);
// Allocate a new touch sensor controller handle
ESP_ERROR_CHECK(touch_sensor_new_controller(&touch_cfg, &sens_handle));
```

To delete the controller handle and free the software and hardware resources, please call `touch_sensor_del_controller`{.interpreted-text role="cpp:func"}. But note that you need to delete the other resources that based on the controller first, like the registered touch channels, otherwise it can\'t be deleted directly.

``` c
ESP_ERROR_CHECK(touch_sensor_del_controller(sens_handle));
```

You can also update the configurations via `touch_sensor_reconfig_controller`{.interpreted-text role="cpp:func"} before the controller is enabled.

``` c
touch_sensor_config_t touch_cfg = {
    // New controller configurations
    // ...
};
ESP_ERROR_CHECK(touch_sensor_reconfig_controller(sens_handle, &touch_cfg));
```

### Touch Sensor Channel Management {#touch-chan}

There are multiple touch channels in the touch sensor module, the touch sensor channel is controlled by the channel handle `touch_channel_handle_t`{.interpreted-text role="cpp:type"}. It can be initialized and allocated by `touch_sensor_new_channel`{.interpreted-text role="cpp:func"}.

``` c
// ...
touch_channel_config_t chan_cfg = {
    // Touch channel configurations
    // ...
};
touch_channel_handle_t chan_handle = NULL;
int chan_id = 0;
// Allocate a new touch sensor controller handle
ESP_ERROR_CHECK(touch_sensor_new_channel(sens_handle, chan_id, &chan_cfg, &chan_handle));
```

To delete the touch channel handle and free the software and hardware resources, please call `touch_sensor_del_channel`{.interpreted-text role="cpp:func"}.

``` c
ESP_ERROR_CHECK(touch_sensor_del_channel(chan_handle));
```

You can also update the configurations via `touch_sensor_reconfig_channel`{.interpreted-text role="cpp:func"} before the controller is enabled.

``` c
touch_channel_config_t chan_cfg = {
    // New touch channel configurations
    // ...
};
ESP_ERROR_CHECK(touch_sensor_reconfig_channel(chan_handle, &chan_cfg));
```

### Filter Configuration {#touch-filter}

The filter can help to increase the stability in different use cases. The filter can be registered by calling `touch_sensor_config_filter`{.interpreted-text role="cpp:func"} and specify the configurations `touch_sensor_filter_config_t`{.interpreted-text role="cpp:type"}. These configurations mainly determine how to filter and update the benchmark and read data. Please note that all touch channels will share this filter.

To deregister the filter, you can call `touch_sensor_config_filter`{.interpreted-text role="cpp:func"} again, and set the second parameter (i.e. `touch_sensor_filter_config_t`{.interpreted-text role="cpp:type"} pointer) to `NULL`.

::: only
esp32

The touch sensor version {IDF_TARGET_TOUCH_SENSOR_VERSION} does not natively support the hardware filter, but the driver can set up a periodically triggered software filter based on `esp_timer`. The interval for the software filter can be specified by `touch_sensor_filter_config_t::interval_ms`{.interpreted-text role="cpp:member"}. Additionally, the `touch_sensor_filter_config_t::data_filter_fn`{.interpreted-text role="cpp:member"} supports to specify a custom filtering function. If there are no special filter requirements, this interface can be set to `NULL` to use the default filter in the driver.
:::

::: only
not esp32

The touch sensor version {IDF_TARGET_TOUCH_SENSOR_VERSION} supports the hardware filter. The filtering and updating strategy for the benchmark can be configured by `touch_sensor_filter_config_t::benchmark`{.interpreted-text role="cpp:member"}, while the filtering of read values can be configured by `touch_sensor_filter_config_t::data`{.interpreted-text role="cpp:member"}.
:::

``` c
// ...
touch_sensor_filter_config_t filter_config = {
    // Filter configurations
    // ...
};
// Register the filter
ESP_ERROR_CHECK(touch_sensor_config_filter(sens_handle, &filter_config));
// ...
// Deregister the filter
ESP_ERROR_CHECK(touch_sensor_config_filter(sens_handle, NULL));
```

### Callback {#touch-callback}

Calling `touch_sensor_register_callbacks`{.interpreted-text role="cpp:func"} to register the touch sensor event callbacks. Once the touch sensor events (like `on_active`, `on_inactive`) trigger, the corresponding callbacks will be invoked, so that to deal with the event in the upper application.

For the general example, when the measured data of the current touch channel exceed the `benchmark` + `active_threshold`, this channel is activated, and the driver will call `on_active` callback to inform the application layer. Similar, when the active channel measured a lower data than `benchmark` + `active_threshold`, then this channel will be inactivated, and `on_inactive` will be called to inform this channel is released.

:::: note
::: title
Note
:::

To ensure the stability of the triggering and releasing, `active_hysteresis` and `debounce_cnt` can be configured to avoid the frequent triggering that caused by jitter and noise.
::::

Please refer to `touch_event_callbacks_t`{.interpreted-text role="cpp:type"} for the details about the supported callbacks.

``` c
touch_event_callbacks_t callbacks = {
    .on_active = example_touch_on_active_cb,
    // Other callbacks
    // ...
};
// Register callbacks
ESP_ERROR_CHECK(touch_sensor_register_callbacks(sens_handle, &callbacks, NULL));

// To deregister callbacks, set the corresponding callback to NULL
callbacks.on_active = NULL;
// Other callbacks to deregister
// ...
ESP_ERROR_CHECK(touch_sensor_register_callbacks(sens_handle, &callbacks, NULL));
```

### Enable and Disable {#touch-enable}

After finished the configuration of the touch controller and touch channels, `touch_sensor_enable`{.interpreted-text role="cpp:func"} can be called to enable the touch sensor controller. It will enter `READY` status and power on the registered channels, then you can start scanning and sampling the touch data. Note that you can only do scanning and reading operation once the controller is enabled. If you want to update the controller or channel configurations, you need to call `touch_sensor_disable`{.interpreted-text role="cpp:func"} first.

``` c
// Enable touch sensor
ESP_ERROR_CHECK(touch_sensor_enable(sens_handle));
// ...
// Disable touch sensor
ESP_ERROR_CHECK(touch_sensor_disable(sens_handle));
```

### Continuous Scan {#touch-conti-scan}

With the touch controller enabled, `touch_sensor_start_continuous_scanning`{.interpreted-text role="cpp:func"} can be called to start the continuous scanning to all the registered touch channels. The read data of these touch channels will be updated automatically in each scan. Calling `touch_sensor_stop_continuous_scanning`{.interpreted-text role="cpp:func"} can stop the continuous scan.

``` c
// Start continuous scan
ESP_ERROR_CHECK(touch_sensor_start_continuous_scanning(sens_handle));
// ...
// Stop continuous scan
ESP_ERROR_CHECK(touch_sensor_stop_continuous_scanning(sens_handle));
```

### Oneshot Scan {#touch-oneshot-scan}

With the touch controller enabled, `touch_sensor_trigger_oneshot_scanning`{.interpreted-text role="cpp:func"} can be called to trigger an one-time scan to all the registered touch channels. Note that oneshot scan is a blocking function, it will keep blocking and only return when the scan is finished. Moreover, you can\'t trigger an oneshot scan after the continuous scan has started.

``` c
// Trigger an oneshot scan with timeout 1000 ms
ESP_ERROR_CHECK(touch_sensor_trigger_oneshot_scanning(sens_handle, 1000));
```

### Read Measurement Data {#touch-read}

Call `touch_channel_read_data`{.interpreted-text role="cpp:func"} to read the data with different types. Like, benchmark, smooth data, etc. You can refer to `touch_chan_data_type_t`{.interpreted-text role="cpp:type"} for the supported data types.

::: only
not esp32 and not esp32s2 and not esp32s3

The {IDF_TARGET_NAME} supports frequency hopping by configuring multiple set of sample configurations, `touch_channel_read_data`{.interpreted-text role="cpp:func"} can read out the data of each sample configuration in a single call, you can determine the sample configuration number by `touch_sensor_config_t::sample_cfg_num`{.interpreted-text role="cpp:member"}, and pass an array (which length is not smaller than the configuration number) to the third parameter `*data`, so that all the measured data of this channel will be stored in the array.
:::

``` c
#define SAMPLE_NUM  1  // Take one sample configuration set for example
uint32_t smooth_data[SAMPLE_NUM] = {};
// Read the smooth data
ESP_ERROR_CHECK(touch_channel_read_data(chan_handle, TOUCH_CHAN_DATA_TYPE_SMOOTH, smooth_data));
```

:::: {#touch-benchmark}
::: only
SOC_TOUCH_SUPPORT_BENCHMARK

### Benchmark Configuration

Normally, you don\'t have to set the benchmark manually, but you can force reset the benchmark to the current smooth value by calling `touch_channel_config_benchmark`{.interpreted-text role="cpp:func"} when necessary.

``` c
touch_chan_benchmark_config_t benchmark_cfg = {
    // Benchmark operations
    // ...
};
ESP_ERROR_CHECK(touch_channel_config_benchmark(chan_handle, &benchmark_cfg));
```
:::
::::

:::: {#touch-waterproof}
::: only
SOC_TOUCH_SUPPORT_WATERPROOF

### Waterproof Configuration

The {IDF_TARGET_NAME} supports waterproof. Waterproof can be registered by calling `touch_sensor_config_waterproof`{.interpreted-text role="cpp:func"} and specify the configurations `touch_waterproof_config_t`{.interpreted-text role="cpp:type"}. There are two parts of the waterproof function:

- Immersion (in-water) proof: `touch_waterproof_config_t::guard_chan`{.interpreted-text role="cpp:member"} can be specified for detecting immersion. It is usually designed as a ring on the PCB, which surrounds all the other touch pads. When this guard ring channel is triggered, that means the touch panel is immersed by water, all the touch channels will stop measuring to avoid falsely triggering.
- Moisture (water-drop) proof: `touch_waterproof_config_t::shield_chan`{.interpreted-text role="cpp:member"} can be specified for detecting moisture. It usually uses the grid layout on the PCB, which covers the whole touch panel. The shield channel will charge and discharge synchronously with the current touch channel, when there is a water droplet covers both shield channel and normal touch channel, `touch_waterproof_config_t::shield_drv`{.interpreted-text role="cpp:member"} can strengthen the electrical coupling caused by the water droplets, and then reconfigure the active threshold based on the disturbance to eliminate the influence that introduced by the water droplet.

To deregister the waterproof function, you can call `touch_sensor_config_waterproof`{.interpreted-text role="cpp:func"} again, and set the second parameter (i.e. `touch_waterproof_config_t`{.interpreted-text role="cpp:type"} pointer) to `NULL`.

``` c
touch_waterproof_config_t waterproof_cfg = {
    // Waterproof configurations
    // ...
};
// Register waterproof function
ESP_ERROR_CHECK(touch_sensor_config_waterproof(sens_handle, &waterproof_cfg));
// ...
// Deregister waterproof function
ESP_ERROR_CHECK(touch_sensor_config_waterproof(sens_handle, NULL));
```
:::
::::

:::::: {#touch-prox-sensing}
::::: only
SOC_TOUCH_SUPPORT_PROX_SENSING

### Proximity Sensing Configuration

The {IDF_TARGET_NAME} supports proximity sensing. Proximity sensing can be registered by calling `touch_sensor_config_proximity_sensing`{.interpreted-text role="cpp:func"} and specify the configurations `touch_proximity_config_t`{.interpreted-text role="cpp:type"}.

::: only
not esp32s2 and not esp32s3

Since the capacitance change caused by proximity sensing is far less than that caused by physical touch, large area of copper foil is often used on PCB to increase the sensing area. In addition, multiple rounds of scans are needed and the result of each scan will be accumulated in the driver to improve the measurement sensitivity. The scan times (rounds) can be determined by `touch_proximity_config_t::scan_times`{.interpreted-text role="cpp:member"} and the charging times of the proximity channel in one scan can be determined by `touch_proximity_config_t::charge_times`{.interpreted-text role="cpp:member"}. Generally, the larger the scan times and charging times is, the higher the sensitivity will be, however, the read data will be unstable if the sensitivity is too high. Proper parameters should be determined regarding the application.
:::

::: only
esp32s2 or esp32s3

Since the capacitance change caused by proximity sensing is far less than that caused by physical touch, large area of copper foil is often used on PCB to increase the sensing area. In addition, multiple rounds of scans are needed and the result of each scan will be accumulated in the driver to improve the measurement sensitivity. The scan times (rounds) can be determined by `touch_proximity_config_t::scan_times`{.interpreted-text role="cpp:member"}. Generally, the larger the scan times and charging times is, the higher the sensitivity will be, however, the read data will be unstable if the sensitivity is too high. Proper parameters should be determined regarding the application.
:::

The accumulated proximity data can be read by `touch_channel_read_data`{.interpreted-text role="cpp:func"} with the data type `TOUCH_CHAN_DATA_TYPE_PROXIMITY`{.interpreted-text role="cpp:enumerator"}

To deregister the proximity sensing, you can call `touch_sensor_config_proximity_sensing`{.interpreted-text role="cpp:func"} again, and set the second parameter (i.e. `touch_proximity_config_t`{.interpreted-text role="cpp:type"} pointer) to `NULL`.

``` c
touch_proximity_config_t prox_cfg = {
    // Proximity sensing configuration
    // ...
};
// Register the proximity sensing
ESP_ERROR_CHECK(touch_sensor_config_proximity_sensing(sens_handle, &prox_cfg));
// ...
// Deregister the proximity sensing
ESP_ERROR_CHECK(touch_sensor_config_proximity_sensing(sens_handle, NULL));
```
:::::
::::::

::::::: {#touch-sleep-wakeup}
:::::: only
SOC_TOUCH_SUPPORT_SLEEP_WAKEUP

### Sleep Wake-up Configuration

The {IDF_TARGET_NAME} supports waking-up the chip from light sleep or deep sleep with the touch sensor as a wake-up source. The wake-up functionality can be registered by calling `touch_sensor_config_sleep_wakeup`{.interpreted-text role="cpp:func"} and specifying the configurations `touch_sleep_config_t`{.interpreted-text role="cpp:type"}.

After registering the touch sensor sleep wake-up, the chip will continue to sample the touch channels after sleep, which will increase the power consumption during the sleep. To reduce the sleep power consumption, you can reduce the number of charging and discharging times, increase the sampling interval, etc.

Moreover, please note that the operations like sampling, wake-up are all done by hardware when the main core is sleeping. Since this driver runs on the main core, it cannot provide functions such as reading or configuring during the sleep.

::: only
SOC_RISCV_COPROC_SUPPORTED

If you want to read or configure the touch sensor during the sleep, you can turn to the driver `components/ulp/ulp_riscv/ulp_core/include/ulp_riscv_touch_ulp_core.h` which based on the `Ultra Low Power (ULP) Coprocessor <../system/ulp>`{.interpreted-text role="doc"}.
:::

::: list
\- Light sleep wake-up: you need to set `slp_wakeup_lvl`{.interpreted-text role="cpp:member"} to `TOUCH_LIGHT_SLEEP_WAKEUP`{.interpreted-text role="cpp:enumerator"} to enable the light sleep wake-up by touch sensor. Note that any registered touch channel can wake-up the chip from light sleep. :esp32: - Deep sleep wake-up: you need to set `slp_wakeup_lvl`{.interpreted-text role="cpp:member"} to `TOUCH_DEEP_SLEEP_WAKEUP`{.interpreted-text role="cpp:enumerator"} to enable the deep sleep wake-up by touch sensor. Note that in version {IDF_TARGET_TOUCH_SENSOR_VERSION}, enabling Deep-sleep wake-up will keep the RTC domain power on during the deep-sleep to maintain the operation of the touch sensor. At this time, any registered touch sensor channels can continue sampling and support waking up from Deep-sleep. :not esp32: - Deep sleep wake-up: beside setting `slp_wakeup_lvl`{.interpreted-text role="cpp:member"} to `TOUCH_DEEP_SLEEP_WAKEUP`{.interpreted-text role="cpp:enumerator"}, you need to specify `deep_slp_chan`{.interpreted-text role="cpp:member"} additionally. In order to reduce the power consumption, only the specified channel can wake-up the chip from the deep sleep when RTC_PREI power domain off. And also, the driver supports to store another set of configurations for the deep sleep via `deep_slp_sens_cfg`{.interpreted-text role="cpp:member"}, this set of configurations only takes effect during the deep sleep, you can customize the configurations to save more power. The configurations will be reset to the previous set after waking-up from the deep sleep. Please be aware that, not only deep sleep wake-up, but also light sleep wake-up will be enabled when the `slp_wakeup_lvl`{.interpreted-text role="cpp:member"} is `TOUCH_DEEP_SLEEP_WAKEUP`{.interpreted-text role="cpp:enumerator"}.
:::

::: only
not esp32

You can decide whether allow to power down RTC_PERIPH domain during the Deep-sleep by `touch_sleep_config_t::deep_slp_allow_pd`{.interpreted-text role="cpp:member"}. If allowed, the RTC_PERIPH domain will be powered down after the chip enters Deep-sleep, and only the specified `touch_sleep_config_t::deep_slp_chan`{.interpreted-text role="cpp:member"} can wake-up the chip from Deep-sleep. If not allowed, all enabled touch channels can wake-up the chip from Deep-sleep.
:::

To deregister the sleep wake-up function, you can call `touch_sensor_config_sleep_wakeup`{.interpreted-text role="cpp:func"} again, and set the second parameter (i.e. `touch_sleep_config_t`{.interpreted-text role="cpp:type"} pointer) to `NULL`.

``` c
touch_sleep_config_t light_slp_cfg = TOUCH_SENSOR_DEFAULT_LSLP_CONFIG();
// Register the light sleep wake-up
ESP_ERROR_CHECK(touch_sensor_config_sleep_wakeup(sens_handle, &light_slp_cfg));
// ...
// Deregister the light sleep wake-up
ESP_ERROR_CHECK(touch_sensor_config_sleep_wakeup(sens_handle, NULL));
// Default Deep-sleep wake-up configurations: RTC_PERIPH will keep power on during the Deep-sleep,
// All enabled touch channel can wake-up the chip from Deep-sleep
touch_sleep_config_t deep_slp_cfg = TOUCH_SENSOR_DEFAULT_DSLP_CONFIG();
// Default Deep-sleep wake-up power down configurations: RTC_PERIPH will be powered down during the Deep-sleep,
// only the specified sleep pad can wake-up the chip from Deep-sleep
// touch_sleep_config_t deep_slp_cfg = TOUCH_SENSOR_DEFAULT_DSLP_PD_CONFIG(sleep_channel, slp_chan_thresh1, ...);
// Register the deep sleep wake-up
ESP_ERROR_CHECK(touch_sensor_config_sleep_wakeup(sens_handle, &deep_slp_cfg));
```
::::::
:::::::

:::: {#touch-denoise-chan}
::: only
SOC_TOUCH_SUPPORT_DENOISE_CHAN

### Denoise Channel Configuration

The {IDF_TARGET_NAME} supports the internal background noise suppression by the denoise channel. Denoise channel can be registered by calling `touch_sensor_config_denoise_channel`{.interpreted-text role="cpp:func"} and specify the configurations `touch_denoise_chan_config_t`{.interpreted-text role="cpp:type"}.

Denoise channel is an internal channel that not fanned out. After the denoise channel is enabled, the sampled data of the other touch channels will minus the data of the denoise channel automatically, so the final measurement result of the touch channels will be attenuated compare to the original data.

Aside of the common touch channel configuration, the reference capacitance that attached to the denoise channel can be set by `touch_denoise_chan_config_t::ref_cap`{.interpreted-text role="cpp:member"}. And the noise suppression resolution can be set by `touch_denoise_chan_config_t::resolution`{.interpreted-text role="cpp:member"}. The higher the resolution, the greater and more accuracy the denoise channel sample data will be, and the better suppression effect it takes. But at the same time, the attenuation of other touch channel sampling values also increases.

For example, the denoise channel resolution is `touch_denoise_chan_resolution_t::TOUCH_DENOISE_CHAN_RESOLUTION_BIT8`{.interpreted-text role="cpp:enumerator"}, i.e., maximum sample data is `255`. Assuming the actual sample data of a normal touch channel is `10000`, and the denoise channel sample data is `100`, then the final measurement result of the touch channel will be `10000 - 100 = 9900`; If we increase the resolution to `touch_denoise_chan_resolution_t::TOUCH_DENOISE_CHAN_RESOLUTION_BIT12`{.interpreted-text role="cpp:enumerator"}, i.e., maximum sample data is `4095`, the resolution is `16` times greater. So the denoise channel sample data will be about `100 * 16 = 1600`, then the final measurement result of this touch channel will be `10000 - 1600 = 8400.`

To deregister the denoise channel, you can call `touch_sensor_config_denoise_channel`{.interpreted-text role="cpp:func"} again, and set the second parameter (i.e. `touch_denoise_chan_config_t`{.interpreted-text role="cpp:type"} pointer) to `NULL`.

``` c
touch_denoise_chan_config_t denoise_cfg = {
    // Denoise channel configurations
    // ...
}
// Register the denoise channel
ESP_ERROR_CHECK(touch_sensor_config_denoise_channel(sens_handle, &denoise_cfg));
// ...
// Deregister the denoise channel
ESP_ERROR_CHECK(touch_sensor_config_denoise_channel(sens_handle, NULL));
```
:::
::::

## Application Examples

> - `peripherals/touch_sensor/touch_sens_basic`{.interpreted-text role="example"} demonstrates how to register touch channels and read the data, including hardware requirements and project configuration instructions.
> - `peripherals/touch_sensor/touch_sens_sleep`{.interpreted-text role="example"} demonstrates how to wake up the chip from the light or deep sleep by the touch sensor.

## Application Notes

### Touch Sensor Power Consumption Issues

Due to the capacitive charging and discharging operation in the touch sensor measurements, it is a relatively high power-consuming peripheral. In applications with high power consumption requirements, the following methods can be helpful to reduce the power consumption.

::: list
- Reduce the number of touch channels: Multiple functions (such as single-press, double-press, long press, etc.) can be multiplexed on the same channel, thereby reducing the number of touch sensors.

\- Increase the measurement interval: By increasing the measurement interval `touch_sensor_config_t::meas_interval_us`{.interpreted-text role="cpp:member"}, the measurement frequency will be reduced, thereby lowering down the power consumption. :esp32: - Reduce single measurement duration: By decreasing the single measurement duration `touch_sensor_sample_config_t::charge_duration_ms`{.interpreted-text role="cpp:member"}, the number of charging and discharging cycles is reduced, resulting in lower power consumption. :not esp32: - Reduce single measurement charging and discharging cycles: By lowering down the single measurement charging and discharging cycles `touch_sensor_sample_config_t::charge_times`{.interpreted-text role="cpp:member"}, power consumption will be decreased. :esp32s2 or esp32s3: - Set the current bias type to self-bias: By configuring `touch_sensor_sample_config_t::bias_type`{.interpreted-text role="cpp:member"} to `touch_bias_type_t::TOUCH_BIAS_TYPE_SELF`{.interpreted-text role="cpp:enumerator"} to use self-bias, which is more power-saving but less stable. :esp32 or esp32s2 or esp32s3: - Lower down the charging and discharging amplitudes: `touch_sensor_sample_config_t::charge_volt_lim_l`{.interpreted-text role="cpp:member"} and `touch_sensor_sample_config_t::charge_volt_lim_h`{.interpreted-text role="cpp:member"} can specify the lower voltage limit during the discharging and the upper voltage limit during the charging. Reducing both voltage limitations and the voltage error between them can also decrease the power consumption. :esp32 or esp32s2 or esp32s3: - Reduce the current bias intensity: Lowering down `touch_channel_config_t::charge_speed`{.interpreted-text role="cpp:member"} (i.e., the current magnitude of the current bias) can help to reduce the power consumption. :not esp32 and not esp32s2 and not esp32s3: - Lower down the LDO voltage biasing intensity: Decreasing `touch_channel_config_t::bias_volt`{.interpreted-text role="cpp:member"} can reduce the power consumption.
:::

## API Reference

::: include-build-file
inc/touch_sens.inc
:::

::: include-build-file
inc/touch_sens_types.inc
:::

::: include-build-file
inc/touch_version_types.inc
:::
