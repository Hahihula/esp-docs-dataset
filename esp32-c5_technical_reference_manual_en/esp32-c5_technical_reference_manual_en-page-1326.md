

```markdown
| PCNT_CHO_NEG_MODE_Un | PCNT_CHO_HCTRL_MODE_Un | Counter Mode |
|----------------------|------------------------|--------------|
|                      |                        |              |
| 1                    | 0                      | Increment    |
|                      | 1                      | Decrement    |
|                      | Others                 | Disable      |
| 2                    | 0                      | Decrement    |
|                      | 1                      | Increment    |
| Others               | N/A                    | Disable      |
```

Each unit has one filter for all its control and input pulse signals. The filter can be enabled with the bit `PCNT_FILTER_EN_Un`. It monitors the signals and ignores all the noise, i.e. the glitches with pulse widths shorter than `PCNT_FILTER_THRESH_Un` APB clock cycles in length.

As shown on Figure 36.2-1, each unit has two channels which process different input pulse signals and increase or decrease values via their respective inc_dec modules, then the two channels send these values to the adder module which has a 16-bit wide signed register. This adder can be suspended by setting `PCNT_CNT_PAUSE_Un`, and cleared by setting `PCNT_PULSE_CNT_RST_Un`.

The PCNT has seven count event watchpoints that share one interrupt. The interrupt can be enabled or disabled by interrupt enable signals of each individual count event watchpoint. Here are the trigger methods for the count events that can be configured and reported by the PCNT, along with their corresponding interrupt events:

*   Maximum count value: When pulse_cnt reaches `PCNT_CNT_H_LIM_Un`, a high limit interrupt is triggered and `PCNT_CNT_THR_H_LIM_LAT_Un` is high.
*   Minimum count value: When pulse_cnt reaches `PCNT_CNT_L_LIM_Un`, a low limit interrupt is triggered and `PCNT_CNT_THR_L_LIM_LAT_Un` is high.
*   Two threshold values: When pulse_cnt equals either `PCNT_CNT_THRES0_Un` or `PCNT_CNT_THRES1_Un`, an interrupt is triggered and either `PCNT_CNT_THRES0_LAT_Un` or `PCNT_CNT_THRES1_LAT_Un` is high respectively.
*   Zero: When pulse_cnt is 0, an interrupt is triggered and `PCNT_CNT_THR_ZERO_LAT_Un` is valid.
*   Upcount Step Threshold: If `PCNT_DALTA_CHANGE_EN_Un` is set to high, when pulse_cnt exceeds `PCNT_CNT_H_STEP_Un` during incrementing, an overflow interrupt is generated, and `PCNT_CNT_THR_H_STEP_LAT_Un` is set to high.

    For example, if `PCNT_CNT_H_STEP_Un` is set to 100, an interrupt will be triggered each time the pulse_cnt reaches integer multiples such as 100, 200, 300, and so on. This type of interrupt can be used to periodically monitor whether the number of input pulses has reached a specified multiple, facilitating functions such as quantitative sampling, data statistics, or regular event handling.

*   Downcount Step Threshold: If `PCNT_DALTA_CHANGE_EN_Un` is set to high, when pulse_cnt falls below `PCNT_CNT_L_STEP_Un` during decrementing, an overflow interrupt is generated, and `PCNT_CNT_THR_L_STEP_LAT_Un` is set to high.

    For example, if `PCNT_DALTA_CHANGE_EN_Un` is set to 100, an interrupt will be triggered each time the pulse_cnt decreases to integer multiples such as 100, 200, 300, and so on. This type of interrupt is
```