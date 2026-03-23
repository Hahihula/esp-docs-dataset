

```markdown
Chapter 13 System Timer (SYSTIMER) GoBack

13.7 Registers

The addresses in this section are relative to system timer base address provided in Table 5.3-2 in Chapter 5 System and Memory.

Register 13.1. SYSTIMER_CONF_REG (0x0000)

[Diagram of register bit field layout with labels]

SYSTIMER_CLK_EN
SYSTIMER_TIMER_UNIT0_WORK_EN
SYSTIMER_TIMER_UNIT1_WORK_EN
SYSTIMER_TIMER_UNIT0_CORE0_STALL_EN
SYSTIMER_TIMER_UNIT1_CORE0_STALL_EN
SYSTIMER_TIMER_UNIT0_CORE1_STALL_EN
SYSTIMER_TIMER_UNIT1_CORE1_STALL_EN
SYSTIMER_TIMER_TARGET0_WORK_EN
SYSTIMER_TIMER_TARGET1_WORK_EN
SYSTIMER_TIMER_TARGET2_WORK_EN

(reserved)

SYSTIMER_ETM_EN (reserved)

Bit field table:

31 30 29 28 27 26 25 24 23 22 21
0   1   0   0   0   1   1   0   0   0   0   ...   0   0   0   0   0   0   0   0   0   0   0   0
Reset

SYSTIMER_ETM_EN Configures whether or not to enable generation of ETM events.
O: Disable
1: Enable
(R/W)

SYSTIMER_TARGET2_WORK_EN Configures whether or not to enable COMP2.
O: Disable
1: Enable
(R/W)

SYSTIMER_TARGET1_WORK_EN Configures whether or not to enable COMP1. See details in SYS-TIMER_TARGET2_WORK_EN. (R/W)

SYSTIMER_TARGET0_WORK_EN Configures whether or not to enable COMPO. See details in SYS-TIMER_TARGET2_WORK_EN. (R/W)

SYSTIMER_TIMER_UNIT1_CORE1_STALL_EN Configures whether or not UNIT1 is stalled when CORE1 is stalled.
O: UNIT1 is not stalled.
1: UNIT1 is stalled.
(R/W)

SYSTIMER_TIMER_UNIT1_CORE0_STALL_EN Configures whether or not UNIT1 is stalled when CORE0 is stalled. See details in SYSTIMER_TIMER_UNIT1_CORE1_STALL_EN. (R/W)

SYSTIMER_TIMER_UNIT0_CORE1_STALL_EN Configures whether or not UNIT0 is stalled when CORE1 is stalled. See details in SYSTIMER_TIMER_UNIT1_CORE1_STALL_EN. (R/W)

SYSTIMER_TIMER_UNIT0_CORE0_STALL_EN Configures whether or not UNIT0 is stalled when CORE0 is stalled. See details in SYSTIMER_TIMER_UNIT1_CORE1_STALL_EN. (R/W)

Continued on the next page...
```