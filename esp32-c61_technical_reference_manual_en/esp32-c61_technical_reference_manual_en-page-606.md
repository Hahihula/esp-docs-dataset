

```markdown
## 12.9 Registers

The addresses in this section are relative to system timer base address provided in Table 4.3-2 in Chapter 4 System and Memory.

Register 12.1. SYSTIMER_CONF_REG (0x0000)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | SYSTIMER_CLK_EN                                                              |
| 30  | SYSTIMER_TIMER_UNIT0_WORK_EN                                                |
| 29  | SYSTIMER_TIMER_UNIT1_WORK_EN                                                |
| 28  | SYSTIMER_TIMER_UNIT0_CORE0_STALL_EN                                         |
| 27  | SYSTIMER_TIMER_UNIT1_CORE0_STALL_EN                                         |
| 26  | SYSTIMER_TIMER_UNIT0_CORE1_STALL_EN                                         |
| 25  | SYSTIMER_TIMER_UNIT1_CORE1_STALL_EN                                         |
| 24  | SYSTIMER_TIMER_TARGET0_WORK_EN                                              |
| 23  | SYSTIMER_TIMER_TARGET1_WORK_EN                                              |
| 22  | SYSTIMER_TIMER_TARGET2_WORK_EN                                              |
| 21  | (reserved)                                                                  |
| 2   | SYSTIMER_ETM_EN                                                             |
| 1   | (reserved)                                                                  |
| 0   | Reset                                                                      |

SYSTIMER_ETM_EN Configures whether to enable generation of ETM events.
O: Disable
1: Enable
(R/W)

SYSTIMER_TARGET2_WORK_EN Configures whether to enable COMP2.
O: Disable
1: Enable
(R/W)

SYSTIMER_TARGET1_WORK_EN Configures whether to enable COMP1. See details in SYS-TIMER_TARGET2_WORK_EN. (R/W)

SYSTIMER_TARGET0_WORK_EN Configures whether to enable COMPO. See details in SYS-TIMER_TARGET2_WORK_EN. (R/W)

SYSTIMER_TIMER_UNIT1_CORE1_STALL_EN Configures whether UNIT1 is stalled when CORE1 is stalled.
O: UNIT1 is not stalled.
1: UNIT1 is stalled.
(R/W)

SYSTIMER_TIMER_UNIT1_CORE0_STALL_EN Configures whether UNIT1 is stalled when CORE0 is stalled. See details in SYSTIMER_TIMER_UNIT1_CORE1_STALL_EN. (R/W)

SYSTIMER_TIMER_UNIT0_CORE1_STALL_EN Configures whether UNIT0 is stalled when CORE1 is stalled. See details in SYSTIMER_TIMER_UNIT1_CORE1_STALL_EN. (R/W)

SYSTIMER_TIMER_UNIT0_CORE0_STALL_EN Configures whether UNIT0 is stalled when CORE0 is stalled. See details in SYSTIMER_TIMER_UNIT1_CORE1_STALL_EN. (R/W)

Continued on the next page...
```