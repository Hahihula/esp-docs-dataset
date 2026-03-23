

```markdown
- SYSTIMER_TIMER_UNITn_WORK_EN: set this bit to enable the counter UNITn in system timer.
- SYSTIMER_TIMER_UNITn_COREO_STALL_EN: if this bit is set, the counter UNITn stops when CPU is stalled. The counter continues its counting after the CPU resumes.

The configuration of the two bits to control the counter UNITn is shown below, assuming that CPU is stalled.

Table 10.4-1. UNITn Configuration Bits

| SYSTIMER_TIMER_UNITn_WORK_EN | SYSTIMER_TIMER_UNITn_COREO_STALL_EN | Counter UNITn |
|------------------------------|--------------------------------------|---------------|
| 0                            | x*                                   | Not at work   |
| 1                            | 1                                    | Stop counting, but will continue its counting after the CPU resumes. |
| 1                            | 0                                    | Keep counting |

x: Don't-care.

When the counter UNITn is at work, the count value is incremented on each counting cycle. When the counter UNITn is stopped, the count value stops increasing and keeps unchanged.

The lower 32 and higher 20 bits of initial count value are loaded from the registers SYSTIMER_TIMER_UNITn_LOAD_LO and SYSTIMER_TIMER_UNITn_LOAD_HI. Writing 1 to the bit SYSTIMER_TIMER_UNITn_LOAD will trigger a reload event, and the current count value will be changed immediately. If UNITn is at work, the counter will continue to count up from the new reloaded value.

Writing 1 to SYSTIMER_TIMER_UNITn_UPDATE will trigger an update event. The lower 32 and higher 20 bits of current count value will be locked into the registers SYSTIMER_TIMER_UNITn_VALUE_LO and SYSTIMER_TIMER_UNITn_VALUE_HI, and then SYSTIMER_TIMER_UNITn_VALUE_VALID is asserted. Before the next update event, the values of SYSTIMER_TIMER_UNITn_VALUE_LO and SYSTIMER_TIMER_UNITn_VALUE_HI remain unchanged.

10.4.2 Comparator and Alarm

The system timer has three 52-bit comparators, shown as COMPx (x = 0, 1, or 2). The comparators can generate independent interrupts based on different alarm values (t) or alarm periods (δt).

Configure SYSTIMER_TARGETx_PERIOD_MODE to choose from the two alarm modes for each COMPx:

- 1: select period mode
- 0: select target mode

In period mode, the alarm period (δt) is provided by the register SYSTIMER_TARGETx_PERIOD. Assuming that current count value is t1, when it reaches (t1 + δt), an alarm interrupt will be generated. Another alarm interrupt also will be generated when the count value reaches (t1 + 2*δt). By such way, periodic alarms are generated.

In target mode, the lower 32 bits and higher 20 bits of the alarm value (t) are provided by SYSTIMER_TIMER_TARGET
```