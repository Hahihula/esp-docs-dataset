

```markdown
## 48.4 Functional Description

The available counter modes of PCNT are as follows:

*   Increment mode: When a channel detects an active edge of sig_ch0_un (can be configured by software), the counter value pulse_cnt increases by 1. Upon reaching PCNT_CNT_H_LIM_Un, pulse_cnt is cleared. If PCNT_CNT_PAUSE_Un is set to 1, then pulse_cnt freezes.
*   Decrement mode: When a channel detects an active edge of sig_ch0_un (can be configured by software), the counter value pulse_cnt decreases by 1. Upon reaching PCNT_CNT_L_LIM_Un, pulse_cnt is cleared. If PCNT_CNT_PAUSE_Un is set to 1, then pulse_cnt freezes.
*   Disable mode: Counting is disabled, and the counter value pulse_cnt freezes.

Table 48.4-1 to Table 48.4-4 provide information on how to configure the counter mode for channel 0.

### Table 48.4-1. Counter Mode. Rising edge of Input Pulse Signal. Control Signal in Low State

| PCNT_CHO_POS_MODE_Un | PCNT_CHO_LCTRL_MODE_Un | Counter Mode |
|----------------------|------------------------|--------------|
|                      |                        |              |
| 0                    | Increment              |              |
| 1                    | Decrement              | Disable      |
| Others               |                        |              |
|                      |                        |              |
| 2                    |                        | Decrement    |
|                      |                        | Increment    |
| Others               |                        | Disable      |
| Others               | N/A                    | Disable      |

### Table 48.4-2. Counter Mode. Rising edge of Input Pulse Signal. Control Signal in High State

| PCNT_CHO_POS_MODE_Un | PCNT_CHO_HCTRL_MODE_Un | Counter Mode |
|----------------------|------------------------|--------------|
|                      |                        |              |
| 0                    | Increment              |              |
| 1                    | Decrement              | Disable      |
| Others               |                        |              |
|                      |                        |              |
| 2                    |                        | Decrement    |
|                      |                        | Increment    |
| Others               |                        | Disable      |
| Others               | N/A                    | Disable      |

### Table 48.4-3. Counter Mode. Falling Edge of Input Pulse Signal. Control Signal in Low State

| PCNT_CHO_NEG_MODE_Un | PCNT_CHO_LCTRL_MODE_Un | Counter Mode |
|----------------------|------------------------|--------------|
|                      |                        |              |
| 0                    | Increment              |              |
| 1                    | Decrement              | Disable      |
| Others               |                        |              |
|                      |                        |              |
| 2                    |                        | Decrement    |
|                      |                        | Increment    |
| Others               |                        | Disable      |
| Others               | N/A                    | Disable      |
```