

```markdown
PCNT_CNT_PAUSE_Un is set to 1 before pulse_cnt reaches PCNT_CNT_H_LIM_Un, then pulse_cnt freezes and its counter mode changes.

*   Decrement mode: When a channel detects an active edge of sig_ch0_un (the active edge can be configured by software), the counter value pulse_cnt decreases by 1. Upon reaching PCNT_CNT_L_LIM_Un, pulse_cnt is cleared. If the channel's counter mode is changed or if PCNT_CNT_PAUSE_Un is set to 1 before pulse_cnt reaches PCNT_CNT_L_LIM_Un, then pulse_cnt freezes and its counter mode changes.
*   Disable mode: Counting is disabled, and the counter value pulse_cnt freezes.

Table 32.2-1 to Table 32.2-4 provide information on how to configure the counter mode for channel 0.

**Table 32.2-1. Counter Mode. Positive Edge of Input Pulse Signal. Control Signal in Low State**

| PCNT_CHO_POS_MODE_Un | PCNT_CHO_LCTRL_MODE_Un | Counter Mode |
| :------------------- | :--------------------- | :----------- |
|                      |                        |              |
| 0                    | Increment              |
| 1                    | Decrement              |
| Others               | Disable                |
| 0                    | Decrement              |
| 2                    | Increment              |
| Others               | Disable                |
| Others               | N/A                    | Disable      |

**Table 32.2-2. Counter Mode. Positive Edge of Input Pulse Signal. Control Signal in High State**

| PCNT_CHO_POS_MODE_Un | PCNT_CHO_HCTRL_MODE_Un | Counter Mode |
| :------------------- | :--------------------- | :----------- |
|                      |                        |              |
| 0                    | Increment              |
| 1                    | Decrement              |
| Others               | Disable                |
| 0                    | Decrement              |
| 2                    | Increment              |
| Others               | Disable                |
| Others               | N/A                    | Disable      |

**Table 32.2-3. Counter Mode. Negative Edge of Input Pulse Signal. Control Signal in Low State**

| PCNT_CHO_NEG_MODE_Un | PCNT_CHO_LCTRL_MODE_Un | Counter Mode |
| :------------------- | :--------------------- | :----------- |
|                      |                        |              |
| 0                    | Increment              |
| 1                    | Decrement              |
| Others               | Disable                |
| 0                    | Decrement              |
| 2                    | Increment              |
| Others               | Disable                |
| Others               | N/A                    | Disable      |
```