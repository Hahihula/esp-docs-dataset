

```markdown
- Monitors the absolute value of the current temperature. Configure TSENS_WAKEUP_TH_LOW and TSENS_WAKEUP_TH_HIGH to set the temperature thresholds. Wake-up will be triggered if the sampled value is above the high threshold or below the low threshold.
- Change value mode:
  - Monitors the temperature changes inside the chip. If the temperature increment of two consecutive samplings exceeds the high threshold configured in TSENS_WAKEUP_TH_HIGH, or the temperature decrement of two consecutive samplings exceeds the low threshold configured in TSENS_WAKEUP_TH_LOW, a wake-up will be triggered. For example, when TSENS_WAKEUP_TH_LOW is set to 8, and the two consecutive sampling values are 28 and 19, resulting in a temperature decrement of 9, a wake-up will be triggered.

## 61.4.4 Temperature Measurement Range and Offset

The temperature sensor is designed with five measurement ranges, as displayed in Table 61.4-1, to enhance accuracy. Each range has its own measurement errors, but users can select particular offsets to obtain calibrated data, so there is no need to be concerned about the errors.

**Table 61.4-1. Temperature Measurement Range and Offset**

| Temperature Measurement Range (°C) | Temperature Offset |
|------------------------------------|--------------------|
| 50 ~ 125                           | -2                 |
| 20 ~ 100                           | -1                 |
| -10 ~ 80                           | 0                  |
| -30 ~ 50                           | 1                  |
| -40 ~ 20                           | 2                  |

## 61.4.5 Data Conversion

The sensor output value (VALUE) is stored in TSENS_OUT. To calculate the actual temperature T (°C) based on VALUE, use the following equation:

```math
T = 0.4386 * VALUE - 27.88 * offset - 20.52
```

where `offset` is the temperature offset displayed in Table 61.4-1.

## 61.5 Event Task Matrix Feature

The temperature sensor on ESP32-P4 supports the Event Task Matrix (ETM) function, which allows the temperature sensor’s ETM tasks to be triggered by any peripherals’ ETM events, or temperature sensor’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to the temperature sensor. For more information, please refer to Chapter 13 Event Task Matrix (ETM).

The temperature sensor can receive the following ETM tasks:
*   TMPSNSR_TASK_START_SAMPLE: The temperature sensor starts sampling when this task is triggered.
*   TMPSNSR_TASK_STOP_SAMPLE: The temperature sensor stops sampling when this task is triggered.

The temperature sensor can generate the following ETM events:
```markdown
Espressif Systems 3014 Submit Documentation Feedback ESP32-P4 TRM PRELIMINARY
```