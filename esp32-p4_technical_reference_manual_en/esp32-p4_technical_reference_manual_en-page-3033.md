

```markdown
tasks. This section introduces the ETM tasks and events related to SAR ADC. For more information, please refer to Chapter 13 Event Task Matrix (ETM).

The SAR ADC can receive the following ETM tasks:

*   `ADC_TASK_SAMPLEO`: LP ADC starts one-shot sampling when this task is triggered.
*   `ADC_TASK_STARTO`: HP ADC starts multi-channel sampling when this task is triggered.
*   `ADC_TASK_STOPO`: SAR ADC stops sampling when this task is triggered.

The SAR ADC can generate the following ETM events:

*   `ADC_EVT_CONV_CMPLTO`: Generated each time SAR ADC completes a sampling in either one-shot sampling mode or multi-channel sampling mode.
*   `ADC_EVT_EQ_ABOVE_THRESHx`: Generated when the HP ADC's filtered data is above the threshold. x = 0, 1, representing threshold monitor 0, 1.
*   `ADC_EVT_EQ_BELOW_THRESHx`: Generated when the HP ADC's filtered data is below the threshold. x = 0, 1, representing threshold monitor 0, 1.
*   `ADC_EVT_STARTEDO`: Generated when SAR ADC begins sampling; one-shot sampling will not trigger this event.
*   `ADC_EVT_STOPPEDO`: Generated when SAR ADC stops sampling, one-shot sampling will not trigger this event.

In practical applications, SAR ADC's ETM events can trigger its own ETM tasks. For example, the `ADC_EVT_EQ_ABOVE_THRESHx` event can trigger the `ADC_TASK_STOPO` task.
```

```markdown
## 62.7 Interrupts

ESP32-P4's SAR ADC can generate the following interrupt signals that will be sent to the Interrupt Matrix.

*   `ADC_INTR`
*   `LP_ADC_INTR`

The following internal interrupt sources from SAR ADC can generate the interrupt signal `ADC_INTR`:

*   `ADC_SARx_DONE_INT`: Triggered when HP `ADCx` completes one sampling.
*   `ADC_THRESx_HIGH_INT`: Triggered when the filtered data is above the high threshold.
*   `ADC_THRESx_LOW_INT`: Triggered when the filtered data is below the low threshold.

The following internal interrupt sources from SAR ADC can generate the interrupt signal `LP_ADC_INTR`:

*   `LPADC_COCPU_SARADCx_DONE_INT`: Triggered when LP `ADCx` completes one sampling.
*   `LPADC_COCPU_SARADCx_ERROR_INT`: Triggered when sampling error occurs.
*   `LPADC_COCPU_SARADCx_WAKE_INT`: Triggered when LP `ADCx` generates a wake-up event (such as conversion data exceeding the threshold).

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 62.9 Register Summary.
```