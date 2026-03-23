

```markdown
Chapter 36 Motor Control PWM (MCPWM)

Register 36.68. MCPWM_UPDATE_CFG_REG (0x010C)
```

```plaintext
(reserved) MCPWM_OP2_FORCE_UP
             MCPWM_OP2_UP_EN
             MCPWM_OPI_UP_EN
             MCPWM_OPO_UP_EN
             MCPWM_GLOBAL_FORCE_UP
             MCPWM_GLOBAL_UP_EN
```

| 31 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----|---|---|---|---|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | Reset |

**MCPWM_GLOBAL_UP_EN** Configures whether to globally update all active registers.
- O: No effect
- 1: Update all active registers globally (R/W)

**MCPWM_GLOBAL_FORCE_UP** Configures whether or not to trigger a forced update of all active registers globally.
- O: No effect
- 1: Trigger a forced update (R/W)

**MCPWM_OPO_UP_EN** Configures whether or not to update active registers in PWM operator O when `MCPWM_GLOBAL_UP_EN` is set to 1.
- O: No effect
- 1: Update active registers in PWM operator O (R/W)

**MCPWM_OPO_FORCE_UP** Configures whether or not to trigger a forced update of active registers in PWM operator O.
- O: No effect
- 1: Trigger a forced update (R/W)

**MCPWM_OP1_UP_EN** Configures whether or not to update active registers in PWM operator 1 when `MCPWM_GLOBAL_UP_EN` is set to 1.
- O: No effect
- 1: Update active registers in PWM operator 1 (R/W)

Continued on the next page...
```