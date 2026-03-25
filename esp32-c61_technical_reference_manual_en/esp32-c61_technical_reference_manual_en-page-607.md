

```markdown
Chapter 12 System Timer

Register 12.1. SYSTIMER_CONF_REG (0x0000)

Continued from the previous page...

SYSTIMER_TIMER_UNIT1_WORK_EN Configures whether to enable UNIT1.
O: Disable
1: Enable
(R/W)

SYSTIMER_TIMER_UNITO_WORK_EN Configures whether to enable UNITO.
O: Disable
1: Enable
(R/W)

SYSTIMER_CLK_EN Configures register clock gating.
O: Only enable needed clock for register read or write operations.
1: Register clock is always enabled for read and write operations.
(R/W)

Register 12.2. SYSTIMER_UNITO_OP_REG (0x0004)
```
```markdown
(reserved) SYSTIMER_TIMER_UNITO_UPDATE SYSTIMER_TIMER_UNITO_VALUE_VALID (reserved)
SYSTIMER_TIMER_UNITO_VALUE_VALID Represents whether UNITO value is synchronized and valid.
O: UNITO value is neither synchronized nor valid
1: UNITO value is synchronized and valid
(R/SS/WTC)

SYSTIMER_TIMER_UNITO_UPDATE Configures whether to update timer UNITO, i.e., reads the UNITO count value to SYSTIMER_TIMER_UNITO_VALUE_HI and SYS-TIMER_TIMER_UNITO_VALUE_LO.
O: No effect
1: Update timer UNITO
(WT)
```