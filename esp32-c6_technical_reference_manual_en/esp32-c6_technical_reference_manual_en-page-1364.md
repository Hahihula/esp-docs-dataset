

```markdown
| -10 ~ 80 | 0 |
|----------|---|
| -30 ~ 50 | 1 |
| -40 ~ 20 | 2 |

## 39.4 Event Task Matrix Feature

The SAR ADC and temperature sensor on ESP32-C6 support the Event Task Matrix (ETM) function, which allows SAR ADC's/temperature sensor's ETM tasks to be triggered by any peripherals' ETM events, or SAR ADC's/temperature sensor's ETM events to trigger any peripherals' ETM tasks. This section introduces the ETM tasks and events related to SAR ADC and temperature sensor. For more information, please refer to Chapter 11 Event Task Matrix (SOC_ETM).

### 39.4.1 SAR ADC's ETM Feature

The SAR ADC can receive the following ETM tasks:

*   `ADC_TASK_SAMPLEO`: ADC starts one-time sampling when this task is triggered.
*   `ADC_TASK_STARTO`: ADC starts continuous sampling when this task is triggered.
*   `ADC_TASK_STOPO`: ADC stops sampling when this task is triggered.

The SAR ADC can generate the following ETM events:

*   `ADC_EVT_CONV_CMPLTO`: Generated when ADC completes a sampling.
*   `ADC_EVT_EQ_ABOVE_THRESHn` (n: 0 ~ 1): Generated when the ADC data is above the threshold.
*   `ADC_EVT_EQ_BELOW_THRESHn` (n: 0 ~ 1): Generated when the ADC data is below the threshold.
*   `ADC_EVT_STARTEDO`: Generated when ADC begins sampling; one-time sampling will not trigger this event.
*   `ADC_EVT_STOPPEDO`: Generated when ADC stops sampling, one-time sampling will not trigger this event.

In practical applications, SAR ADC's ETM events can trigger its own ETM tasks. For example, the `ADC_EVT_EQ_ABOVE_THRESHn` event can trigger the `ADC_TASK_STOPO` task.

### 39.4.2 Temperature Sensor's ETM Feature

The temperature sensor can receive the following ETM tasks:

*   `TMPNSNR_TASK_START_SAMPLE`: The temperature sensor starts sampling when this task is triggered.
*   `TMPNSNR_TASK_STOP_SAMPLE`: The temperature sensor stops sampling when this task is triggered.

The temperature sensor can generate the following ETM events:

*   `TMPNSNR_EVT_OVER_LIMIT`: Generated when the temperature is beyond the threshold.
```