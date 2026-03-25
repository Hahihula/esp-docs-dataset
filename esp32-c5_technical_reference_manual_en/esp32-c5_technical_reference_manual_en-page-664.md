

```markdown
When the counter UNITn is at work, the count value is incremented on each counting cycle. When the counter UNITn is stopped, the count value stops increasing and keeps unchanged.

The lower 32 and higher 20 bits of the initial count value are loaded from the registers SYSTIMER_TIMER_UNITn_LOAD_LO and SYSTIMER_TIMER_UNITn_LOAD_HI. Writing 1 to the bit SYSTIMER_TIMER_UNITn_LOAD will trigger a reload event, and the current count value will be changed immediately. If UNITn is at work, the counter will continue to count up from the new reloaded value.

Writing 1 to SYSTIMER_TIMER_UNITn_UPDATE will trigger an update event. The lower 32 and higher 20 bits of the current count value will be locked into the registers SYSTIMER_TIMER_UNITn_VALUE_LO and SYSTIMER_TIMER_UNITn_VALUE_HI, and then SYSTIMER_TIMER_UNITn_VALUE_VALID is asserted. Before the next update event, the values of SYSTIMER_TIMER_UNITn_VALUE_LO and SYSTIMER_TIMER_UNITn_VALUE_HI remain unchanged.

## 14.5.2 Comparator and Alarm

The system timer has three 52-bit comparators, shown as COMPx (x = 0, 1, or 2). The comparators can generate independent interrupts based on different alarm values (t) or alarm periods (δt).

Configure SYSTIMER_TARGETx_PERIOD_MODE to choose from the two alarm modes for each COMPx:

*   1: period mode
*   0: target mode

In period mode, the alarm period (δt) is provided by the register SYSTIMER_TARGETx_PERIOD. Assuming that current count value is t1, when it reaches (t1 + δt), an alarm interrupt will be generated. When the count value reaches (t1 + 2×δt), another alarm interrupt also will be generated. By such way, periodic alarms are generated.

In target mode, the lower 32 bits and higher 20 bits of the alarm value (t) are provided by SYSTIMER_TIMER_TARGETx_LO and SYSTIMER_TIMER_TARGETx_HI. Assuming that current count value is t2 (t2 <= t), an alarm interrupt will be generated when the count value reaches the alarm value (t). Unlike in period mode, only one alarm interrupt is generated in target mode.

SYSTIMER_TARGETx_TIMER_UNIT_SEL is used to choose the count value from which timer counter to be compared to generate alarms:

*   1: Use the count value from UNIT1
*   0: Use the count value from UNIT0

Finally, set SYSTIMER_TARGETx_WORK_EN and COMPx starts to compare the count value:

*   In target mode, COMPx compares it with the alarm value (t).
*   In period mode, COMPx compares it with the alarm period (t1 + n×δt).

An alarm is generated when the count value equals to the alarm value (t) in target mode or to the start value + n×δt (n = 1, 2, 3...) in period mode. But if the alarm value (t) set in registers is less than the current count value, i.e., the target has already passed, when the current count value is larger than the alarm value (t) within a range (0 ~ 2^51 - 1), an alarm interrupt will also be generated immediately. No matter in target mode or period mode, the low 32 bits and high 20 bits of the real alarm value can always be read from SYSTIMER_TARGETx_LO_RO and SYSTIMER_TARGETx_HI_RO. The alarm trigger point and the relationship between current count value t_c and the alarm value t_t are shown below.
```