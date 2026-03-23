

```markdown
## 10.7 Registers

The addresses in this section are relative to system timer base address provided in Table 3.3-3 in Chapter 3 System and Memory.

Register 10.1. SYSTIMER_CONF_REG (0x0000)

| Bit | Description |
|-----|-------------|
| 31  | reserved    |
| 30  | SYSTIMER_CLK_EN | Register clock gating. 1: Register clock is always enabled for read and write operations. 0: Only enable needed clock for register read or write operations. (R/W) |
| 29  | SYSTIMER_TIMER_UNITO_WORK_EN | UNITO work enable bit. (R/W) |
| 28  | SYSTIMER_TIMER_UNIT1_WORK_EN | UNIT1 work enable bit. (R/W) |
| 27  | SYSTIMER_TIMER_UNITO_COREO_STALL_EN | UNITO is stalled when CPU stalled. (R/W) |
| 26  | SYSTIMER_TIMER_UNIT1_COREO_STALL_EN | UNIT1 is stalled when CPU stalled. (R/W) |
| 25  | SYSTIMER_TARGET0_WORK_EN | COMPO work enable bit. (R/W) |
| 24  | SYSTIMER_TARGET1_WORK_EN | COMP1 work enable bit. (R/W) |
| 23  | SYSTIMER_TARGET2_WORK_EN | COMP2 work enable bit. (R/W) |
| 22-0| reserved    |

SYSTIMER_CLK_EN Register clock gating. 1: Register clock is always enabled for read and write operations. 0: Only enable needed clock for register read or write operations. (R/W)

SYSTIMER_TIMER_UNITO_WORK_EN UNITO work enable bit. (R/W)

SYSTIMER_TIMER_UNIT1_WORK_EN UNIT1 work enable bit. (R/W)

SYSTIMER_TIMER_UNITO_COREO_STALL_EN UNITO is stalled when CPU stalled. (R/W)

SYSTIMER_TIMER_UNIT1_COREO_STALL_EN UNIT1 is stalled when CPU stalled. (R/W)

SYSTIMER_TARGET0_WORK_EN COMPO work enable bit. (R/W)

SYSTIMER_TARGET1_WORK_EN COMP1 work enable bit. (R/W)

SYSTIMER_TARGET2_WORK_EN COMP2 work enable bit. (R/W)
```