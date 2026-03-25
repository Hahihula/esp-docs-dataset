

```markdown
- APB_SARADC_THRESx_LOW_INT: Triggered when the filtered data is below the low threshold of monitor x.
```

## 40.8 Event Task Matrix Feature

The SAR ADC on ESP32-H2 support the Event Task Matrix (ETM) function, which allows SAR ADC’s ETM tasks to be triggered by any peripherals’ ETM events, or SAR ADC’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to SAR ADC. For more information, please refer to Chapter 10 Event Task Matrix (SOC_ETM).

The SAR ADC can receive the following ETM tasks:

- `ADC_TASK_SAMPLEO`: ADC starts one-shot sampling when this task is triggered.
- `ADC_TASK_STARTO`: ADC starts multi-channel sampling when this task is triggered.
- `ADC_TASK_STOPO`: ADC stops sampling when this task is triggered.

The SAR ADC can generate the following ETM events:

- `ADC_EVT_CONV_CMPLTO`: Generated each time ADC completes a sampling in either one-shot sampling mode or multi-channel sampling mode.
- `ADC_EVT_EQ_ABOVE_THRESHx`: Generated when the ADC filtered data is above the threshold. x = 0, 1, representing threshold monitor 0, 1.
- `ADC_EVT_EQ_BELOW_THRESHx`: Generated when the ADC filtered data is below the threshold. x = 0, 1, representing threshold monitor 0, 1.
- `ADC_EVT_STARTEDO`: Generated when ADC begins sampling; one-shot sampling will not trigger this event.
- `ADC_EVT_STOPPEDO`: Generated when ADC stops sampling, one-shot sampling will not trigger this event.

In practical applications, SAR ADC’s ETM events can trigger its own ETM tasks. For example, the `ADC_EVT_EQ_ABOVE_THRESHx` event can trigger the `ADC_TASK_STOPPO` task.
```