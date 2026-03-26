

```markdown
2. Software reads the corresponding bit `SYSTIMER_TIMER_UNITn_VALUE_VALID` to be valid to confirm synchronization is done.
3. Software reads the corresponding status registers `SYSTIMER_TIMER_UNITn_VALUE_HI` and `SYSTIMER_TIMER_UNITn_VALUE_LO`.

## 15.6 Interrupts

ESP32-P4’s system timer can generate the following interrupt signals that will be sent to the **Interrupt Matrix**.

- `SYSTIMER_TARGETO_INT`
- `SYSTIMER_TARGET1_INT`
- `SYSTIMER_TARGET2_INT`

There are several internal interrupt sources from the system timer that can generate the above interrupt signals. The interrupt sources from the system timer are listed with their trigger conditions and the resulted interrupt signals in Table 15.6-1.

### Table 15.6-1. System Timer’s Internal Interrupt Sources

| Internal Interrupt Source | Trigger Condition           | Interrupt Signal               |
|---------------------------|-----------------------------|--------------------------------|
| SYSTIMER_INTO             | When COMP0 alarms           | SYSTIMER_TARGETO_INT          |
| SYSTIMER_INT1             | When COMP1 alarms           | SYSTIMER_TARGET1_INT          |
| SYSTIMER_INT2             | When COMP2 alarms           | SYSTIMER_TARGET2_INT          |

The above interrupts are level-type alarm interrupts. The interrupt signal is asserted high when the comparator starts to alarm. Until the software clears the interrupt, it remains high. To enable interrupts, set the bit `SYSTIMER_TARGETx_INT_ENA`.

**Note:**

For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 12 *Interrupt Matrix* > Section 12.2 *Interrupt Terminology in ESP32-P4*.

Each interrupt source can be configured by a common set of registers that are described in Section *Interrupt Configuration Registers*. The specific registers can be found in Section 15.8 *Register Summary*.

## 15.7 Programming Procedure

When configuring `COMPx` and `UNITn`, please ensure the corresponding COMP and UNIT are at work.

### 15.7.1 Read Current Count Value

1. Set `SYSTIMER_TIMER_UNITn_UPDATE` to fill the current count value of `COMPx` into `SYSTIMER_TIMER_UNITn_VALUE_HI` and `SYSTIMER_TIMER_UNITn_VALUE_LO`.
```