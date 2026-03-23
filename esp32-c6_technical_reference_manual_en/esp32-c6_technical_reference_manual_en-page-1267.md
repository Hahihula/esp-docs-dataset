

```markdown
## Register 36.44. MCPWM_GEN2_STMP_CFG_REG (0x00AC)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 10  | MCPWM_GEN2_B_SHDW_FULL      | Set and reset by hardware.<br>0: B's active reg has been updated with shadow register latest value. <br>1: PWM generator 2 time stamp B's shadow reg is filled and waiting to be transferred to B's active reg. (R/SC/WTC) |
| 9   | MCPWM_GEN2_A_SHDW_FULL      | Set and reset by hardware.<br>0: A's active reg has been updated with shadow register latest value. <br>1: PWM generator 2 time stamp A's shadow reg is filled and waiting to be transferred to A's active reg. (R/SC/WTC) |
| 7   | MCPWM_GEN2_B_UPMETHOD       | Configures update method for PWM generator 2 time stamp B's active register. See details in MCPWM_GEN2_A_UPMETHOD. (R/W) |
| 4   | MCPWM_GEN2_A_UPMETHOD       | Configures update method for PWM generator 2 time stamp A's active register.<br>When all bits are set to 0: immediately.<br>When bit0 is set to 1: TEZ<br>When bit1 is set to 1: TEP<br>When bit2 is set to 1: sync<br>When bit3 is set to 1: disable the update (R/W) |
| 3   | —                           | (reserved)                                                                  |
| 0   | Reset                       |                                                                             |

## Register 36.45. MCPWM_GEN2_TSTMP_A_REG (0x00BO)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 16  | MCPWM_GEN2_A                | Shadow register for PWM generator 2 time stamp A. (R/W)                      |
```