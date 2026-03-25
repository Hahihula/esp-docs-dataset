

```markdown
| Bit Field | Description |
|-----------|-------------|
| (reserved) |             |
| MCPWM_GEN1_B_SHDW_FULL | Configures whether or not the value in the shadow register is written to the corresponding active register at a specific time. This field is set and reset by hardware. O: Write the latest value in the shadow register to B's active register 1: Write the value to the PWM generator 1 time stamp B's shadow register, and wait to be transferred to A's active register (R/W) |
| MCPWM_GEN1_A_SHDW_FULL | Configures whether or not the value in the shadow register is written to the corresponding active register at a specific time. This field is set and reset by hardware. O: Write the latest value in the shadow register to A's active register 1: Write the value to the PWM generator 1 time stamp A's shadow register, and wait to be transferred to A's active register (R/W) |
| MCPWM_GEN1_A_UPMETHOD | Configures update method for PWM generator 1 time stamp A's active register. When all bits are set to 0: immediately. When bit0 is set to 1: TEZ. When bit1 is set to 1: TEP When bit2 is set to 1: sync When bit3 is set to 1: disable the update (R/W) |
| MCPWM_GEN1_B_UPMETHOD | Configures update method for PWM generator 1 time stamp B's active register. See details in MCPWM_GEN1_A_UPMETHOD. (R/W) |
```

Register 36.30. `MCPWM_GEN1_STMP_CFG_REG` (0x0074)

```markdown
| Bit | Description |
|-----|-------------|
| 31  |             |
|     | Reset        |
| 10-9| MCPWM_GEN1_B_SHDW_FULL |
| 8   | MCPWM_GEN1_A_SHDW_FULL |
| 7   | MCPWM_GEN1_B_UPMETHOD |
| 4   | MCPWM_GEN1_A_UPMETHOD |
```

MCPWM_GEN1_A_UPMETHOD Configures update method for PWM generator 1 time stamp A's active register.
When all bits are set to 0: immediately. When bit0 is set to 1: TEZ.
When bit1 is set to 1: TEP
When bit2 is set to 1: sync
When bit3 is set to 1: disable the update (R/W)

MCPWM_GEN1_B_UPMETHOD Configures update method for PWM generator 1 time stamp B's active register. See details in MCPWM_GEN1_A_UPMETHOD. (R/W)

MCPWM_GEN1_A_SHDW_FULL Configures whether or not the value in the shadow register is written to the corresponding active register at a specific time. This field is set and reset by hardware.
O: Write the latest value in the shadow register to A's active register
1: Write the value to the PWM generator 1 time stamp A's shadow register, and wait to be transferred to A's active register (R/SC/WTC)

MCPWM_GEN1_B_SHDW_FULL Configures whether or not the value in the shadow register is written to the corresponding active register at a specific time. This field is set and reset by hardware.
O: Write the latest value in the shadow register to B's active register
1: Write the value to the PWM generator 1 time stamp B's shadow register, and wait to be transferred to A's active register (R/SC/WTC)

Register 36.31. `MCPWM_GEN1_TSTMP_A_REG` (0x0078)

```markdown
| Bit | Description |
|-----|-------------|
| 31  |             |
|     | Reset        |
```

MCPWM_GEN1_A Shadow register for PWM generator 1 time stamp A. (R/W)
```