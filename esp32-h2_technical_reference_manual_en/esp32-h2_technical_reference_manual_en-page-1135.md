

```markdown
## Register 36.44. MCPWM_GEN2_STMP_CFG_REG (0x00AC)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 10  | MCPWM_GEN2_B_SHDW_FULL         |                                                                             |
| 9   | MCPWM_GEN2_A_SHDW_FULL         |                                                                             |
| 7   | MCPWM_GEN2_A_UPMETHOD          | Configures update method for PWM generator 2 time stamp A's active register. When all bits are set to 0: immediately.<br>When bit0 is set to 1: TEZ<br>When bit1 is set to 1: TEP<br>When bit2 is set to 1: sync<br>When bit3 is set to 1: disable the update (R/W) |
| 4   | MCPWM_GEN2_B_UPMETHOD          | Configures update method for PWM generator 2 time stamp B's active register. See details in MCPWM_GEN2_A_UPMETHOD. (R/W) |
| 3   | MCPWM_GEN2_A_SHDW_FULL         | Configures whether or not the value in the shadow register is written to the corresponding active register at a specific time. This field is set and reset by hardware.<br>0: Write the latest value in the shadow register to A's active register<br>1: Write the value to the PWM generator 2 time stamp A's shadow register, and wait to be transferred to A's active register (R/SC/WTC) |
| 0   | MCPWM_GEN2_B_SHDW_FULL         | Configures whether or not the value in the shadow register is written to the corresponding active register at a specific time. This field is set and reset by hardware.<br>0: Write the latest value in the shadow register to B's active register<br>1: Write the value to the PWM generator 2 time stamp B's shadow register, and wait to be transferred to A's active register (R/SC/WTC) |

## Register 36.45. MCPWM_GEN2_TSTMP_A_REG (0x00BO)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 16  | MCPWM_GEN2_A                   | Shadow register for PWM generator 2 time stamp A. (R/W)                      |
```