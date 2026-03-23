

```markdown
Register 36.16. MCPWM_GENO_STMP_CFG_REG (0x003C)
```

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30-24|                                | (reserved)                                                                  |
| 23  | MCPWM_GENO_B_SHDW_FULL         | Set and reset by hardware.                                                 |
| 22  | MCPWM_GENO_A_SHDW_FULL         | Set and reset by hardware.                                                 |
| 21  | MCPWM_GENO_B_UPMETHOD          | Configures the update method for PWM generator 0 time stamp B's active register. (R/W) |
| 20  | MCPWM_GENO_A_UPMETHOD          | Configures the update method for PWM generator 0 time stamp A's active register. (R/W) |
| 19-8|                                | (reserved)                                                                  |
| 7   |                                | When bit0 is set to 1: TEZ                                                 |
| 6   |                                | When bit1 is set to 1: TEP                                                 |
| 5   |                                | When bit2 is set to 1: Sync                                                |
| 4   |                                | When bit3 is set to 1: Disable the update                                 |

MCPWM_GENO_A_UPMETHOD Configures the update method for PWM generator 0 time stamp A's active register.
- When all bits are set to 0: Immediately
- When bit0 is set to 1: TEZ
- When bit1 is set to 1: TEP
- When bit2 is set to 1: Sync
- When bit3 is set to 1: Disable the update (R/W)

MCPWM_GENO_B_UPMETHOD Configures the update method for PWM generator 0 time stamp B's active register. (R/W)
- When all bits are set to 0: Immediately
- When bit0 is set to 1: TEZ
- When bit1 is set to 1: TEP
- When bit2 is set to 1: Sync
- When bit3 is set to 1: Disable the update (R/W)

MCPWM_GENO_A_SHDW_FULL Set and reset by hardware.
0: A's active reg has been updated with shadow register latest value.
1: PWM generator 0 time stamp A's shadow reg is filled and waiting to be transferred to A's active reg. (R/SC/WTC)

MCPWM_GENO_B_SHDW_FULL Set and reset by hardware.
0: B's active reg has been updated with shadow register latest value.
1: PWM generator 0 time stamp B's shadow reg is filled and waiting to be transferred to B's active reg. (R/SC/WTC)
```