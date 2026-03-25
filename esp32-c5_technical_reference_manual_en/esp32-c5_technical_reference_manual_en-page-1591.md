

```markdown
Register 41.28. MCPWM_UPDATE_CFG_REG (0x010C)
```

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | Reset |

**MCPWM_GLOBAL_UP_EN** Configures whether to globally update all active registers.

- O: No effect
- 1: Update all active registers globally (R/W)

**MCPWM_GLOBAL_FORCE_UP** Configures whether to trigger a forced update of all active registers globally.

- O: No effect
- 1: Trigger a forced update (R/W)

**MCPWM_OPO_UP_EN** Configures whether to update active registers in PWM operator 0 when `MCPWM_GLOBAL_UP_EN` is set to 1.

- O: No effect
- 1: Update active registers in PWM operator 0 (R/W)

**MCPWM_OPO_FORCE_UP** Configures whether to trigger a forced update of active registers in PWM operator 0.

- O: No effect
- 1: Trigger a forced update (R/W)

**MCPWM_OP1_UP_EN** Configures whether to update active registers in PWM operator 1 when `MCPWM_GLOBAL_UP_EN` is set to 1.

- O: No effect
- 1: Update active registers in PWM operator 1 (R/W)

Continued on the next page...
```