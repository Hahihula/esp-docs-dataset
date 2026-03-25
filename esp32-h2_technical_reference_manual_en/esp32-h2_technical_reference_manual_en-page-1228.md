

```markdown
5. Wait for 100 µs (so that the output value gradually approaches the actual temperature) and then read the data from `APB_SARADC_TSENS_OUT`.

To enable hardware-triggered automatic temperature monitoring, add the following programming steps before powering up the sensor:

1. Configure `APB_SARADC_TSENS_SAMPLE_RATE` to set sampling rate.
2. Configure `APB_SARADC_WAKEUP_MODE` to select wake-up mode for temperature monitoring.
3. Configure `APB_SARADC_WAKEUP_TH_HIGH/LOW` to set the high and low temperature monitoring thresholds.
4. Set `APB_SARADC_WAKEUP_EN` to start temperature monitoring.
5. Set `APB_SARADC_TSENS_SAMPLE_EN` to enable automatic temperature monitoring.

In automatic temperature monitoring mode, the output value will not be stored. However, users can get the value anytime from `APB_SARADC_TSENS_OUT`.

## 39.6 Interrupts

*   `APB_SARADC_TSENS_INT`: Triggered when the temperature sample value exceeds the threshold.

## 39.7 Event Task Matrix Feature

The temperature sensor on ESP32-H2 support the Event Task Matrix (ETM) function, which allows temperature sensor’s ETM tasks to be triggered by any peripherals’ ETM events, or temperature sensor’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to temperature sensor. For more information, please refer to Chapter 10 Event Task Matrix (SOC_ETM).

The temperature sensor can receive the following ETM tasks:

*   `TMPSNSR_TASK_START_SAMPLE`: The temperature sensor starts sampling when this task is triggered.
*   `TMPSNSR_TASK_STOP_SAMPLE`: The temperature sensor stops sampling when this task is triggered.

The temperature sensor can generate the following ETM events:

*   `TMPSNSR_EVT_OVER_LIMIT`: Generated when the temperature is beyond the threshold.

In practical applications, temperature sensor’s ETM events can trigger its own ETM tasks.

For example, the `TMPSNSR_EVT_OVER_LIMIT` event can trigger the `TMPSNSR_TASK_STOP_SAMPLE` task.
```