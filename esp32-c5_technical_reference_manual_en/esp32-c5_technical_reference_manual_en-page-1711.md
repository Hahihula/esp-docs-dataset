

```markdown
Figure 46.5-8. DMA Data Format

data    12-bit ADC conversion result
ch_sel  3-bit channel information


## 46.6 Event Task Matrix Feature

The SAR ADC on ESP32-C5 supports the Event Task Matrix (ETM) function, which allows SAR ADC’s ETM tasks to be triggered by any peripherals’ ETM events, or SAR ADC’s ETM events to trigger any peripherals’ ETM tasks. This section introduces the ETM tasks and events related to SAR ADC and temperature sensor. For more information, please refer to Chapter 12 Event Task Matrix (ETM).

The SAR ADC can receive the following ETM tasks:

*   `ADC_TASK_SAMPLE0`: ADC starts one-shot sampling when this task is triggered.
*   `ADC_TASK_STARTO`: ADC starts multi-channel sampling when this task is triggered.
*   `ADC_TASK_STOPO`: ADC stops sampling when this task is triggered.

The SAR ADC can generate the following ETM events:

*   `ADC_EVT_CONV_CMPLTO`: Generated each time ADC completes a sampling in either one-shot sampling mode or multi-channel sampling mode.
*   `ADC_EVT_EQ_ABOVE_THRESHx`: Generated when the ADC filtered data is above the threshold. x = 0, 1, representing threshold monitor 0, 1.
*   `ADC_EVT_EQ_BELOW_THRESHx`: Generated when the ADC filtered data is below the threshold. x = 0, 1, representing threshold monitor 0, 1.
*   `ADC_EVT_STARTEDO`: Generated when ADC begins sampling; one-shot sampling will not trigger this event.
*   `ADC_EVT_STOPPEDO`: Generated when ADC stops sampling, one-shot sampling will not trigger this event.

In practical applications, SAR ADC’s ETM events can trigger its own ETM tasks. For example, the `ADC_EVT_EQ_ABOVE_THRESHx` event can trigger the `ADC_TASK_STOPO` task.


## 46.7 Interrupts

ESP32-C5’s SAR ADC can generate the APB_ADC_INTR interrupt signal that will be sent to the Interrupt Matrix. The following internal interrupt sources from SAR ADC can generate the interrupt signal APB_ADC_INTR:

*   `APB_SARADC_ADC_DONE_INT`: Triggered when SAR ADC completes one conversion.
*   `APB_SARADC_THRESx_HIGH_INT`: Triggered when the filtered data is above the high threshold of monitor x.
*   `APB_SARADC_THRESx_LOW_INT`: Triggered when the filtered data is below the low threshold of monitor x.
```