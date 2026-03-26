

```markdown
Chapter 15 System Timer

GoBack

15.5 Functional Description

Figure 15.5-1 shows the procedure to generate alarm in system timer. In this process, one timer counter and one timer comparator are used. An alarm interrupt will be generated accordingly based on the comparison result in the comparator.

15.5.1 Counter

The system timer has two 52-bit timer counters, shown as UNITn (n = 0 or 1). Their counting clock source is a 16 MHz clock, i.e., CNT_CLK. Whether UNITn works or not is controlled by three bits in register SYSTIMER_CONF_REG:

*   SYSTIMER_TIMER_UNITn_WORK_EN: set this bit to enable the counter UNITn in the system timer.
*   SYSTIMER_TIMER_UNITn_CORE0_STALL_EN: if this bit is set, the counter UNITn stops when CPU0 is stalled. The counter continues its counting after the CPU resumes.
*   SYSTIMER_TIMER_UNITn_CORE1_STALL_EN: if this bit is set, the counter UNITn stops when CPU1 is stalled. The counter continues its counting after the CPU resumes.

The configuration of the bits to control the counter UNITn is shown below, assuming that CPU is stalled.

Table 15.5-1. UNITn Configuration Bits

| SYSTIMER_TIMER_UNITn_WORK_EN | SYSTIMER_TIMER_UNITn_CORE0_STALL_EN | SYSTIMER_TIMER_UNITn_CORE1_STALL_EN | Counter UNITn |
|------------------------------|--------------------------------------|--------------------------------------|---------------|
| 0                            | x*                                   | x*                                   | Not at work   |
| 1                            | 1                                    | x                                    | Stop counting, but will continue its counting after the CPU0 resumes |
| 1                            | x                                    | 1                                    | Stop counting, but will continue its counting after the CPU1 resumes |
| 1                            | 0                                    | 0                                    | Keep counting |

*   x: Don’t-care.
```