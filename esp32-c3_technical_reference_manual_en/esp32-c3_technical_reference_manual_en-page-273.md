
```markdown
Chapter 10 System Timer (SYSTIMER)

x_LO and SYSTIMER_TIMER_TARGETx_HI. Assuming that current count value is t2 (t2 <= t), an alarm interrupt will be generated when the count value reaches the alarm value (t). Unlike in period mode, only one alarm interrupt is generated in target mode.

SYSTIMER_TARGETx_TIMER_UNIT_SEL is used to choose the count value from which timer counter to be compared for alarm:

* 1: use the count value from UNIT1
* 0: use the count value from UNIT0

Finally, set SYSTIMER_TARGETx_WORK_EN and COMPx starts to compare the count value with the alarm value (t) in target mode or with the alarm period (t1 + n*tδt) in period mode.

An alarm is generated when the count value equals to the alarm value (t) in target mode or to the start value + n*alarm period δt (n = 1,2,3...) in period mode. But if the alarm value (t) set in registers is less than current count value, i.e. the target has already passed, or current count value is larger than the target value (t) within a range (0 ~ 2^51 - 1), an alarm interrupt also is generated immediately. The relationship between current count value tc, the alarm value tt and alarm trigger point is shown below.

Table 10.4-2. Trigger Point

| Relationship Between tc and tt | Trigger Point |
|--------------------------------|---------------|
| tc - tt <= 0                   | tc = tt, an alarm is triggered. |
| 0 <= (tc - tt) < 2^51 - 1      | An alarm is triggered immediately.<br>(tc < 2^51 and tt < 2^51,<br>or tc >= 2^51 and tt >= 2^51) |
| tc - tt >= 2^51 - 1            | tc overflows after counting to its maximum value 52'hfffffffffffff, and then starts counting up from 0.<br>When its value reaches tt, an alarm is triggered. |

10.4.3 Synchronization Operation

The clock (APB_CLK) used in software operation is not the same one as the timer counters and comparators working on CNT_CLK. Synchronization is needed for some configuration registers. A complete synchronization action takes two steps:

1. Software writes suitable values to configuration fields, see the first column in Table 10.4-3.
2. Software writes 1 to corresponding bits to start synchronization, see the second column in Table 10.4-3.

Table 10.4-3. Synchronization Operation

| Configuration Fields                     | Synchronization Enable Bit |
|------------------------------------------|----------------------------|
| SYSTIMER_TIMER_UNITn_LOAD_LO             | SYSTIMER_TIMER_UNITn_LOAD |
| SYSTIMER_TIMER_UNITn_LOAD_HI             |                            |
| SYSTIMER_TARGETx_PERIOD                  |                            |
| SYSTIMER_TIMER_TARGETx_HI                | SYSTIMER_TIMER_COMPx_LOAD |
| SYSTIMER_TIMER_TARGETx_LO                |                            |

Espressif Systems
273
ESP32-C3 TRM (Version 1.3)
Submit Documentation Feedback
```