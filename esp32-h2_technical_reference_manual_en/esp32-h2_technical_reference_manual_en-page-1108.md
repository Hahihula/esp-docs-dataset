

```markdown
Register 36.16. MCPWM_GENO_STMP_CFG_REG (0x003C)
```

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30-24|                                | (reserved)                                                                  |
| 10  | MCPWM_GENO_B_SHDW_FULL        | Configures whether or not the value in the shadow register is written to the corresponding active register at a specific time. This field is set and reset by hardware.<br>0: Write the latest value in the shadow register to B's active register<br>1: Write the value to the PWM generator 0 time stamp B's shadow register, and wait to be transferred to B's active register (R/SC/WTC) |
| 9   | MCPWM_GENO_B_UPMETHOD         | Configures the update method for PWM generator 0 time stamp B's active register. (R/W)<br>When all bits are set to 0: Immediately<br>When bit0 is set to 1: TEZ<br>When bit1 is set to 1: TEP<br>When bit2 is set to 1: Sync<br>When bit3 is set to 1: Disable the update (R/W) |
| 8   | MCPWM_GENO_A_SHDW_FULL         | Configures whether or not the value in the shadow register is written to the corresponding active register at a specific time. This field is set and reset by hardware.<br>0: Write the latest value in the shadow register to A's active register<br>1: Write the value to the PWM generator 0 time stamp A's shadow register, and wait to be transferred to A's active register (R/SC/WTC) |
| 7   | MCPWM_GENO_A_UPMETHOD          | Configures the update method for PWM generator 0 time stamp A's active register. (R/W)<br>When all bits are set to 0: Immediately<br>When bit0 is set to 1: TEZ<br>When bit1 is set to 1: TEP<br>When bit2 is set to 1: Sync<br>When bit3 is set to 1: Disable the update (R/W) |
| 6-4 |                                | (reserved)                                                                  |
| 3   |                                | (reserved)                                                                  |
| 2   |                                | (reserved)                                                                  |
| 1   |                                | (reserved)                                                                  |
| 0   | Reset                          |                                                                             |

MCPWM_GENO_A_UPMETHOD Configures the update method for PWM generator 0 time stamp A's active register.
When all bits are set to 0: Immediately
When bit0 is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: Sync
When bit3 is set to 1: Disable the update (R/W)

MCPWM_GENO_B_UPMETHOD Configures the update method for PWM generator 0 time stamp B's active register. (R/W)
When all bits are set to 0: Immediately
When bit0 is set to 1: TEZ
When bit1 is set to 1: TEP
When bit2 is set to 1: Sync
When bit3 is set to 1: Disable the update (R/W)

MCPWM_GENO_A_SHDW_FULL Configures whether or not the value in the shadow register is written to the corresponding active register at a specific time. This field is set and reset by hardware.
0: Write the latest value in the shadow register to A's active register
1: Write the value to the PWM generator 0 time stamp A's shadow register, and wait to be transferred to A's active register (R/SC/WTC)

MCPWM_GENO_B_SHDW_FULL Configures whether or not the value in the shadow register is written to the corresponding active register at a specific time. This field is set and reset by hardware.
0: Write the latest value in the shadow register to B's active register.
1: Write the value to the PWM generator 0 time stamp B's shadow register, and wait to be transferred to B's active register. (R/SC/WTC)
```