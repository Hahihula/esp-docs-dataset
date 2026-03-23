

```markdown
| PCNT_CHO_POS_MODE_Un | PCNT_CHO_LCTRL_MODE_Un | Counter Mode |
|----------------------:|------------------------:|:-------------|
|                      1|                        0| Increment    |
|                      1|                        1| Decrement    |
|                      1|                     Others| Disable      |
|                      2|                        0| Decrement    |
|                      2|                        1| Increment    |
|                      2|                     Others| Disable      |
| Others               |                       N/A| Disable      |

Table 31.2-2. Counter Mode. Positive Edge of Input Pulse Signal. Control Signal in High State

| PCNT_CHO_POS_MODE_Un | PCNT_CHO_HCTRL_MODE_Un | Counter Mode |
|----------------------:|------------------------:|:-------------|
|                      0|                        0| Increment    |
|                      1|                        1| Decrement    |
|                      Others|                     Others| Disable      |
|                      2|                        0| Decrement    |
|                      2|                        1| Increment    |
|                      Others|                       N/A| Disable      |

- Decrement mode: When a channel detects an active edge of sig_ch0_un (can be configured by software), the counter value pulse_cnt decreases by 1. Upon reaching PCNT_CNT_L_LIM_Un, pulse_cnt is cleared. If the channel's counter mode is changed or if PCNT_CNT_PAUSE_Un is set before pulse_cnt reaches PCNT_CNT_L_LIM_Un, then pulse_cnt freezes and its counter mode changes.
- Disable mode: Counting is disabled, and the counter value pulse_cnt freezes.

Table 31.2-1 to Table 31.2-4 provide information on how to configure the counter mode for channel 0.

Each unit has one filter for all its control and input pulse signals. A filter can be enabled with the bit PCNT_FILTER_EN_Un. The filter monitors the signals and ignores all the noise, i.e. the glitches with pulse widths shorter than PCNT_FILTER_THRES_Un APB clock cycles in length.

As shown on Figure 31.2-1, each unit has two channels which process different input pulse signals and increase or decrease values via their respective inc_dec modules, then the two channels send these values

Table 31.2-3. Counter Mode. Negative Edge of Input Pulse Signal. Control Signal in Low State

| PCNT_CHO_NEG_MODE_Un | PCNT_CHO_LCTRL_MODE_Un | Counter Mode |
|----------------------:|------------------------:|:-------------|
|                      1|                        0| Increment    |
|                      1|                        1| Decrement    |
|                      1|                     Others| Disable      |
|                      2|                        0| Decrement    |
|                      2|                        1| Increment    |
|                      2|                     Others| Disable      |
| Others               |                       N/A| Disable      |
```