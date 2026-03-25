

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

Each unit has one filter for all its control and input pulse signals. The filter can be enabled with the bit `PCNT_FILTER_EN_Un`. It monitors the signals and ignores all the noise, i.e., the glitches with pulse widths shorter than `PCNT_FILTER_THRESH_Un` APB clock cycles in length.

As shown on Figure 32.2-1, each unit has two channels which process different input pulse signals and increase or decrease values via their respective inc_dec modules, then the two channels send these values to the adder module which has a 16-bit wide signed register. This adder can be suspended by setting `PCNT_CNT_PAUSE_Un`, and cleared by setting `PCNT_PULSE_CNT_RST_Un`.

The PCNT has five watchpoints that share one interrupt. The interrupt can be enabled or disabled by interrupt enable signals of each individual watchpoint.

*   Maximum count value: When pulse_cnt is greater than or equal to `PCNT_CNT_H_LIM_Un`, a high limit interrupt is triggered and `PCNT_CNT_THR_H_LIM_LAT_Un` is high.
*   Minimum count value: When pulse_cnt is less than or equal to `PCNT_CNT_L_LIM_Un`, a low limit interrupt is triggered and `PCNT_CNT_THR_L_LIM_LAT_Un` is high.
*   Two threshold values: When pulse_cnt equals either `PCNT_CNT_THRES0_Un` or `PCNT_CNT_THRES1_Un`, an interrupt is triggered and either `PCNT_CNT_THRES0_LAT_Un` or `PCNT_CNT_THRES1_LAT_Un` is high.
*   Zero: When pulse_cnt is 0, an interrupt is triggered and `PCNT_CNT_THRES_ZERO_LAT_Un` is valid.

If `PCNT_CNT_H_LIM_Un` and/or `PCNT_CNT_L_LIM_Un` are reconfigured by software when PCNT is working, the new configuration will take effect after pulse_cnt counts to any of the above five watchpoints; if `PCNT_CNT_THRES0_Un` and/or `PCNT_CNT_THRES1_Un` are reconfigured by software, the new configuration will take effect immediately.

## 32.3 Applications

In each unit, channel 0 and channel 1 can be configured to work independently or together. The three subsections below provide details of channel 0 incrementing independently, channel 0 decrementing independently, and channel 0 and channel 1 incrementing together. For other working modes not elaborated in this section (e.g., channel 1 incrementing/decrementing independently, or one channel incrementing while the other decrementing), reference can be made to these three subsections.
```