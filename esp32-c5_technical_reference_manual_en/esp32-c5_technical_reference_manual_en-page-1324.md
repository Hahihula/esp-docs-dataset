

```markdown
## 36.2 Functional Description

Figure 36.2-1 shows PCNT’s architecture. As stated above, `ctrl_ch0_un` is the control signal for ch0 of unit n. Its high and low states can be assigned with different counter modes to count the channel’s input pulse signal `sig_ch0_un` on negative or positive edges. The available counter modes are as follows:

*   Increment mode: When a channel detects an active edge of `sig_ch0_un` (the active edge can be configured by software), the counter value `pulse_cnt` increases by 1. Upon reaching `PCNT_CNT_H_LIM_Un`, `pulse_cnt` is cleared. If the channel’s counter mode is changed or if `PCNT_CNT_PAUSE_Un` is set to 1 before `pulse_cnt` reaches `PCNT_CNT_H_LIM_Un`, then `pulse_cnt` freezes and its counter mode changes.
*   Decrement mode: When a channel detects an active edge of `sig_ch0_un` (the active edge can be configured by software), the counter value `pulse_cnt` decreases by 1. Upon reaching
```