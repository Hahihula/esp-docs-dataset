

```markdown
Register 56.8. MCPWM_GENn_STMP_CFG_REG (n: 0-2) (0x003C+0x38*n)

| Bit Field | Description |
|-----------|-------------|
| (reserved)|             |
| 10        | MCPWM_CMPRn_B_SHDW_FULL |
| 9         | MCPWM_PWM_CMPRn_A_SHDW_FULL |
| 8         | MCPWM_CMPRn_B_UPMETHOD |
| 7         | MCPWM_CMPRn_A_UPMETHOD |
| 3-4       | Reset |

MCPWM_CMPRn_A_UPMETHOD Configures the update method for PWM generator n time stamp A's active register.
When all bits are set to 0: Immediately
When bitO is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: Sync
When bit3 is set to 1: Disable the update (R/W)

MCPWM_CMPRn_B_UPMETHOD Configures the update method for PWM generator n time stamp B's active register.
When all bits are set to 0: Immediately
When bitO is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: Sync
When bit3 is set to 1: Disable the update (R/W)

MCPWM_CMPRn_A_SHDW_FULL Configures whether the value in the shadow register is written to the corresponding active register at a specific time. This field is set and reset by hardware.
0: Write the latest value in the shadow register to A's active register
1: Write the value to the PWM generator n time stamp A's shadow register, and wait to be transferred to A's active register (R/SC/WTC)

MCPWM_CMPRn_B_SHDW_FULL Configures whether the value in the shadow register is written to the corresponding active register at a specific time. This field is set and reset by hardware.
0: Write the latest value in the shadow register to B's active register
1: Write the value to the PWM generator n time stamp B's shadow register, and wait to be transferred to B's active register (R/SC/WTC)
```