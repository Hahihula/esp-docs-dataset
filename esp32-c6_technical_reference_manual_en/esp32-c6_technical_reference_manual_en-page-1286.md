

```markdown
Chapter 36 Motor Control PWM (MCPWM)

Register 36.68. MCPWM_UPDATE_CFG_REG (0x010C)

Continued from the previous page...

MCPWM_OP1_FORCE_UP Configures whether or not to trigger a forced update of active registers in PWM operator 1.
O: No effect
1: Trigger a forced update
(R/W)

MCPWM_OP2_UP_EN Configures whether or not to update active registers in PWM operator 2 when MCPWM_GLOBAL_UP_EN is set to 1.
O: No effect
1: Update active registers in PWM operator 2
(R/W)

MCPWM_OP2_FORCE_UP Configures whether or not to trigger a forced update of active registers in PWM operator 2.
O: No effect
1: Trigger a forced update
(R/W)
```