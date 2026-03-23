

```markdown
Figure 39.2-1. SAR ADCs Function Overview

As shown in Figure 39.2-1, the SAR ADC module provides the following functions and consists of the following components:

*   Measures voltages from up to seven channels.
*   Clock management: selects clock sources and their dividers:
    *   Clock sources: can be XTAL_CLK, RC_FAST_CLK, or PLL_F80M_CLK;
    *   Divided Clocks:
        *   SAR_CLK: operating clock for SAR ADC and Digital_reader (the control signal generator for analog circuit). Note that the divider (sar_div) of SAR_ADC must be no less than 15;
        *   ADC_CTRL_CLK: operating clock for DIG ADC FSM and other logic circuits except for APB interface and Digital_reader.
*   Digital_reader (driven by DIG ADC FSM): reads data from SAR ADC.
*   DIG ADC FSM: generates the signals required throughout the ADC sampling process.
*   Threshold monitorx: threshold monitor 1 and threshold monitor 2. The monitorx will trigger an interrupt when the sampled value is greater than the pre-set high threshold or less than the pre-set low threshold.

The following sections describe the individual components in details.
```