

```markdown
When SYSTIMER_ETM_EN is set to 1, the alarm pulses can trigger the ETM event.

## 12.4.4 Synchronization Operation

The clock (APB_CLK) used in software operation is different from the clock (CNT_CLK) driving timer counters and comparators. Therefore, some configuration registers need to be synchronized. A complete synchronization action takes two steps:

1. Software writes specific values to configuration fields, see the first column in Table 12.4-3.
2. Software writes 1 to corresponding bits to start synchronization, see the second column in Table 12.4-3.

Table 12.4-3. Synchronization Operation for Configuration Registers

| Configuration Fields | Synchronization Enable Bit |
|----------------------|----------------------------|
| SYSTIMER_TIMER_UNITn_LOAD_LO | SYSTIMER_TIMER_UNITn_LOAD |
| SYSTIMER_TIMER_UNITn_LOAD_HI |                            |
| SYSTIMER_TARGETx_PERIOD |                            |
| SYSTIMER_TIMER_TARGETx_HI | SYSTIMER_TIMER_COMPx_LOAD |
| SYSTIMER_TIMER_TARGETx_LO |                            |

Synchronization is also needed for reading some status registers since the timer counter related status have a different clock from APB_CLK. A complete synchronization action takes three steps:

1. Software writes 1 to the updating register `SYSTIMER_TIMER_UNITn_UPDATE`.
2. Software reads the corresponding bit `SYSTIMER_TIMER_UNITn_VALUE_VALID` to be valid to confirm synchronization is done.
3. Software reads the corresponding status registers `SYSTIMER_TIMER_UNITn_VALUE_HI` and `SYSTIMER_TIMER_UNITn_VALUE_LO`.

## 12.4.5 Interrupt

Each comparator has one alarm interrupt respectively, named as `SYSTIMER_TARGETx_INT`. The interrupt signal is asserted high when the comparator starts to alarm. Until any software clears the interrupt, it remains high. To enable interrupts, set the bit `SYSTIMER_TARGETx_INT_ENA`.

## 12.5 Programming Procedure

When configuring COMPx and UNITn, please ensure the corresponding COMP and UNIT are at work.

### 12.5.1 Read Current Count Value

1. Set `SYSTIMER_TIMER_UNITn_UPDATE` to fill the current count value of COMPx into `SYSTIMER_TIMER_UNITn_VALUE_HI` and `SYSTIMER_TIMER_UNITn_VALUE_LO`.
2. Poll the reading of `SYSTIMER_TIMER_UNITn_VALUE_VALID` till it's 1. Then, user can read the count value from `SYSTIMER_TIMER_UNITn_VALUE_HI` and `SYSTIMER_TIMER_UNITn_VALUE_LO`.
```