

```markdown
1. Software writes specific values to configuration fields, see the first column in Table 13.4-3.
2. Software writes 1 to corresponding bits to start synchronization, see the second column in Table 13.4-3.

Table 13.4-3. Synchronization Operation for Configuration Registers

| Configuration Fields | Synchronization Enable Bit |
|----------------------|----------------------------|
| SYSTIMER_TIMER_UNITn_LOAD_LO<br>SYSTIMER_TIMER_UNITn_LOAD_HI | SYSTIMER_TIMER_UNITn_LOAD |
| SYSTIMER_TARGETx_PERIOD<br>SYSTIMER_TIMER_TARGETx_HI<br>SYSTIMER_TIMER_TARGETx_LO | SYSTIMER_TIMER_COMPx_LOAD |

Synchronization is also needed for reading some status registers since the timer counter related status have a different clock than APB_CLK. A complete synchronization action takes three steps:

1. Software writes specific values to the updating register `SYSTIMER_TIMER_UNITn_UPDATE`.
2. Software reads the corresponding bit `SYSTIMER_TIMER_UNITn_VALUE_VALID` to be valid to check synchronization is done.
3. Software reads corresponding status registers `SYSTIMER_TIMER_UNITn_VALUE_HI` and `SYSTIMER_TIMER_UNITn_VALUE_LO`.

13.4.5 Interrupt

Each comparator has one level-type alarm interrupt, named as `SYSTIMER_TARGETx_INT`. Interrupts signal is asserted high when the comparator starts to alarm. Until the interrupt is cleared by software, it remains high. To enable interrupts, set the bit `SYSTIMER_TARGETx_INT_ENA`.

13.5 Programming Procedure

When configuring COMPx and UNITn, please ensure the corresponding COMP and UNIT are at work.

13.5.1 Read Current Count Value

1. Set `SYSTIMER_TIMER_UNITn_UPDATE` to update the current count value of COMPx into `SYSTIMER_TIMER_UNITn_VALUE_HI` and `SYSTIMER_TIMER_UNITn_VALUE_LO`.
2. Poll the reading of `SYSTIMER_TIMER_UNITn_VALUE_VALID` till it's 1. Then, user can read the count value from `SYSTIMER_TIMER_UNITn_VALUE_HI` and `SYSTIMER_TIMER_UNITn_VALUE_LO`.
3. Read the lower 32 bits and higher 20 bits from `SYSTIMER_TIMER_UNITn_VALUE_LO` and `SYSTIMER_TIMER_UNITn_VALUE_HI` respectively.

13.5.2 Configure One-Time Alarm in Target Mode

1. Set `SYSTIMER_TARGETx_TIMER_UNIT_SEL` to select the counter (UNIT0 or UNIT1) used for COMPx.
```