---
original_file_path: api-reference/peripherals/temp_sensor.rst
---

# Temperature Sensor

`zh_CN:[中文]`{.interpreted-text role="link_to_translation"}

## Introduction

The {IDF_TARGET_NAME} has a built-in sensor used to measure the chip\'s internal temperature. The temperature sensor module contains an 8-bit Sigma-Delta analog-to-digital converter (ADC) and a digital-to-analog converter (DAC) to compensate for the temperature measurement.

:::: note
::: title
Note
:::

The temperature sensor is designed primarily to measure the temperature **inside** the silicon. The sensor can reflect the temperature changes very well but it can\'t give a precise measurement value. So it\'s not recommended to use it for ambient temperature measurement.
::::

## Functional Overview

The description of the temperature sensor functionality is divided into the following sections:

::: list
- `temp-resource-allocation`{.interpreted-text role="ref"} - covers which parameters should be set up to get a temperature sensor handle and how to recycle the resources when the temperature sensor finishes working.
- `temp-enable-and-disable-temperature-sensor`{.interpreted-text role="ref"} - covers how to enable and disable the temperature sensor.

\- `temp-get-temperature-value`{.interpreted-text role="ref"} - covers how to get the real-time temperature value. :SOC_TEMPERATURE_SENSOR_INTR_SUPPORT: - `temp-install-temperature-threshold-callback`{.interpreted-text role="ref"} - describes how to register a temperature threshold callback. - `temp-power-management`{.interpreted-text role="ref"} - covers how the temperature sensor is affected when changing power mode (e.g., Light-sleep mode). :SOC_TEMPERATURE_SENSOR_INTR_SUPPORT: - `temp-iram-safe`{.interpreted-text role="ref"} - describes tips on how to make the temperature sensor interrupt work better along with a disabled cache. - `temp-thread-safety`{.interpreted-text role="ref"} - covers how to make the driver to be thread-safe. :SOC_TEMPERATURE_SENSOR_SUPPORT_ETM: - `temperature-sensor-etm-event-and-task`{.interpreted-text role="ref"} - describes what the events and tasks can be connected to the ETM channel.
:::

### Resource Allocation {#temp-resource-allocation}

The {IDF_TARGET_NAME} has just one built-in temperature sensor hardware. The temperature sensor instance is represented by `temperature_sensor_handle_t`{.interpreted-text role="cpp:type"}, which is also the bond of the context. By using `temperature_sensor_handle_t`{.interpreted-text role="cpp:type"}, the temperature sensor properties can be accessed and modified in different function calls to control and manage the temperature sensor. The variable would always be the parameter of the temperature APIs with the information of hardware and configurations, so you can just create a pointer of type `temperature_sensor_handle_t`{.interpreted-text role="cpp:type"} and passing to APIs as needed.

In order to install a built-in temperature sensor instance, the first thing is to evaluate the temperature range in your detection environment. For example, if the testing environment is in a room, the range you evaluate might be 10 °C \~ 30 °C; if the testing in a lamp bulb, the range you evaluate might be 60 °C \~ 110 °C. Based on that, configuration structure `temperature_sensor_config_t`{.interpreted-text role="cpp:type"} should be defined in advance:

- `range_min`{.interpreted-text role="cpp:member"}: The minimum value of the testing range you have evaluated.
- `range_max`{.interpreted-text role="cpp:member"}: The maximum value of the testing range you have evaluated.
- `allow_pd`{.interpreted-text role="cpp:member"} configures if the driver allows the system to power down the peripheral in light sleep mode. Before entering sleep, the system will backup the temperature sensor register context, which will be restored later when the system exit the sleep mode. Powering down the peripheral can save more power, but at the cost of more memory consumed to save the register context. It\'s a tradeoff between power consumption and memory consumption. This configuration option relies on specific hardware feature, if you enable it on an unsupported chip, you will see error message like `not able to power down in light sleep`.

After the ranges are set, the structure could be passed to `temperature_sensor_install`{.interpreted-text role="cpp:func"}, which will instantiate the temperature sensor instance and return a handle.

As mentioned above, different measure ranges have different measurement errors. You do not need to care about the measurement error because we have an internal mechanism to choose the minimum error according to the given range.

If the temperature sensor is no longer needed, you need to call `temperature_sensor_uninstall`{.interpreted-text role="cpp:func"} to free the temperature sensor resource.

#### Creating a Temperature Sensor Handle

- Step 1: Evaluate the testing range. In this example, the range is 20 °C \~ 50 °C.
- Step 2: Configure the range and obtain a handle.

``` c
temperature_sensor_handle_t temp_handle = NULL;
temperature_sensor_config_t temp_sensor_config = TEMPERATURE_SENSOR_CONFIG_DEFAULT(20, 50);
ESP_ERROR_CHECK(temperature_sensor_install(&temp_sensor_config, &temp_handle));
```

### Enable and Disable Temperature Sensor {#temp-enable-and-disable-temperature-sensor}

1.  Enable the temperature sensor by calling `temperature_sensor_enable`{.interpreted-text role="cpp:func"}. The internal temperature sensor circuit will start to work. The driver state will transit from init to enable.
2.  To Disable the temperature sensor, please call `temperature_sensor_disable`{.interpreted-text role="cpp:func"}.

### Get Temperature Value {#temp-get-temperature-value}

After the temperature sensor is enabled by `temperature_sensor_enable`{.interpreted-text role="cpp:func"}, you can get the current temperature by calling `temperature_sensor_get_celsius`{.interpreted-text role="cpp:func"}.

``` c
// Enable temperature sensor
ESP_ERROR_CHECK(temperature_sensor_enable(temp_handle));
// Get converted sensor data
float tsens_out;
ESP_ERROR_CHECK(temperature_sensor_get_celsius(temp_handle, &tsens_out));
printf("Temperature in %f °C\n", tsens_out);
// Disable the temperature sensor if it is not needed and save the power
ESP_ERROR_CHECK(temperature_sensor_disable(temp_handle));
```

::: only
SOC_TEMPERATURE_SENSOR_INTR_SUPPORT

### Install Temperature Threshold Callback {#temp-install-temperature-threshold-callback}

{IDF_TARGET_NAME} supports automatically triggering to monitor the temperature value continuously. When the temperature value reaches a given threshold, an interrupt will happen. Thus you can install your own interrupt callback functions to do what they want, e.g., alarm, restart, etc. The following information indicates how to prepare a threshold callback.

- `temperature_sensor_event_callbacks_t::on_threshold`{.interpreted-text role="cpp:member"}: As this function is called within the ISR context, you must ensure that the function does not attempt to block, e.g., by making sure that only FreeRTOS APIs with the `ISR` suffix are called from within the function, etc. The function prototype is declared in `temperature_thres_cb_t`{.interpreted-text role="cpp:type"}.

You can save your own context to `temperature_sensor_register_callbacks`{.interpreted-text role="cpp:func"} as well, via the parameter `user_arg`. The user data will be directly passed to the callback function.

``` c
IRAM_ATTR static bool temp_sensor_monitor_cbs(temperature_sensor_handle_t tsens, const temperature_sensor_threshold_event_data_t *edata, void *user_data)
{
    ESP_DRAM_LOGI("tsens", "Temperature value is higher or lower than threshold, value is %d\n...\n\n", edata->celsius_value);
    return false;
}

// Callback configurations
temperature_sensor_abs_threshold_config_t threshold_cfg = {
    .high_threshold = 50,
    .low_threshold = -10,
};
// Set absolute value monitor threshold.
temperature_sensor_set_absolute_threshold(temp_sensor, &threshold_cfg);
// Register interrupt callback
temperature_sensor_event_callbacks_t cbs = {
    .on_threshold = temp_sensor_monitor_cbs,
};
// Install temperature callback.
temperature_sensor_register_callbacks(temp_sensor, &cbs, NULL);
```
:::

::: only
not SOC_TEMPERATURE_SENSOR_INTR_SUPPORT
:::

### Power Management

As the temperature sensor does not use the APB clock, it will keep working no matter if the power management is enabled with `CONFIG_PM_ENABLE`.

::: only
SOC_TEMPERATURE_SENSOR_INTR_SUPPORT

### IRAM Safe {#temp-iram-safe}

By default, the temperature sensor interrupt will be deferred when the cache is disabled for reasons like writing/erasing flash. Thus the event callback functions will not get executed in time, which is not expected in a real-time application.

There is a Kconfig option `CONFIG_TEMP_SENSOR_ISR_IRAM_SAFE`{.interpreted-text role="ref"} that will:

1.  Enable the interrupt that is being serviced even when the cache is disabled.
2.  Place all functions that are used by the ISR into IRAM.

This allows the interrupt to run while the cache is disabled but comes at the cost of increased IRAM consumption.
:::

::: only
not SOC_TEMPERATURE_SENSOR_INTR_SUPPORT
:::

### Thread Safety

In the temperature sensor driver, we do not add any protection to ensure the thread safety, because typically this driver is only supposed to be used in one task. If you have to use this driver in different tasks, please add extra locks to protect it.

::::: only
SOC_TEMPERATURE_SENSOR_SUPPORT_ETM

### ETM Event and Task {#temperature-sensor-etm-event-and-task}

Temperature Sensor is able to generate events that can interact with the `ETM </api-reference/peripherals/etm>`{.interpreted-text role="doc"} module. The supported events are listed in the `temperature_sensor_etm_event_type_t`{.interpreted-text role="cpp:type"}. You can call `temperature_sensor_new_etm_event`{.interpreted-text role="cpp:func"} to get the corresponding ETM event handle. The supported tasks are listed in the `temperature_sensor_etm_task_type_t`{.interpreted-text role="cpp:type"}. You can call `temperature_sensor_new_etm_task`{.interpreted-text role="cpp:func"} to get the corresponding ETM task handle.

:::: note
::: title
Note
:::

- `TEMPERATURE_SENSOR_EVENT_OVER_LIMIT`{.interpreted-text role="cpp:enumerator"} for `temperature_sensor_etm_event_type_t::event_type`{.interpreted-text role="cpp:member"} depends on what kind of threshold you set first. If you set the absolute threshold by `temperature_sensor_set_absolute_threshold`{.interpreted-text role="cpp:func"}, then the `TEMPERATURE_SENSOR_EVENT_OVER_LIMIT`{.interpreted-text role="cpp:enumerator"} refers to absolute threshold. Likewise, if you set the delta threshold by `temperature_sensor_set_delta_threshold`{.interpreted-text role="cpp:func"}, then the `TEMPERATURE_SENSOR_EVENT_OVER_LIMIT`{.interpreted-text role="cpp:enumerator"} refers to delta threshold.
::::

For how to connect the event and task to an ETM channel, please refer to the `ETM </api-reference/peripherals/etm>`{.interpreted-text role="doc"} documentation.
:::::

## Unexpected Behaviors

1.  The value you get from the chip is usually different from the ambient temperature. It is because the temperature sensor is built inside the chip. To some extent, it measures the temperature of the chip.

2.  When installing the temperature sensor, the driver may print `the boundary you gave cannot meet the range of internal temperature sensor`. It is because the built-in temperature sensor has a testing limit. The error comes from the incorrect configuration of `temperature_sensor_config_t`{.interpreted-text role="cpp:type"} as follow:

    > (1) Totally out of range, like 200 °C \~ 300 °C.
    > (2) Cross the boundary of each predefined measurement. like 40 °C \~ 110 °C.

## Application Examples

- `peripherals/temperature_sensor/temp_sensor`{.interpreted-text role="example"} demonstrates how to use the built-in temperature sensor, showcasing the measurement range and error based on different DAC levels and offsets.

::: only
SOC_TEMPERATURE_SENSOR_INTR_SUPPORT

- `peripherals/temperature_sensor/temp_sensor_monitor`{.interpreted-text role="example"} demonstrates how to use the temperature sensor to automatically monitor temperature values continuously, triggering an interrupt when a specific value is reached or when the change between two consecutive samplings is larger/smaller than the settings.
:::

## API Reference

::: include-build-file
inc/temperature_sensor.inc
:::

::: include-build-file
inc/temperature_sensor_types.inc
:::

:::: only
SOC_TEMPERATURE_SENSOR_SUPPORT_ETM

::: include-build-file
inc/temperature_sensor_etm.inc
:::
::::
