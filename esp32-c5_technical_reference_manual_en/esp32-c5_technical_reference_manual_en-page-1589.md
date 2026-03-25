

```markdown
Register 41.24. MCPWM_CAP_TIMER_PHASE_REG (0x00EC)

31                                 0                                 Reset
+-------------------------------------------------------------------------------------------------+
|                                                                                                  |
+-------------------------------------------------------------------------------------------------+

MCPWM_CAP_PHASE Configures phase value for capture timer sync operation.
(R/W)


Register 41.25. MCPWM_CAP_CHn_CFG_REG (n: 0-2) (0x00F0+0x4*n)

31                                 13 12 11 10                                  3   2   1   0
+-------------------------------------------------------------------------------------------------------------------------------+
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |
+-------------------------------------------------------------------------------------------------------------------------------+

MCPWM_CAPn_EN Configures whether to enable capture on channel n.
O: Disable
1: Enable
(R/W)

MCPWM_CAPn_MODE Configures the edge of capture on channel O after prescaling.
When bitO is set to 1: enable capture on the falling edge.
When bit1 is set to 1: enable capture on the rising edge.
(R/W)

MCPWM_CAPn_PRESCALE Configures the prescale value on the rising edge of CAPO. Prescale
value = PWM_CAPO_PRESCALE + 1. (R/W)

MCPWM_CAPn_IN_INVERT Configures whether to invert CAPn from GPIO matrix before prescale.
O: Normal
1: Invert
(R/W)

MCPWM_CAPn_SW Configures whether to trigger a software-forced capture on channel O.
O: Not trigger
1: Trigger
(WT)
```