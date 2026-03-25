

```markdown
Register 11.56. PMU_IMM_I2C_ISO_REG (0x00E8)

| 31 | 30 | 29 | ... | 0 |
|----:|----:|----:|-----|---|
|   0 |   0 |   0 | ... |   0 |

PMU_TIE_HIGH_I2C_ISO_EN Configures whether to force the PMU I2C_ISO enabling signal to high.
- O: No effect
- 1: Force to high (WT)

PMU_TIE_LOW_I2C_ISO_EN Configures whether to force the PMU I2C_ISO enabling signal to low.
- O: No effect
- 1: Force to low (WT)

Register 11.57. PMU_POWER_WAIT_TIMERO_REG (0x00EC)

| 31 | 23 | 22 | ... | 4 | 0 |
|----:|----:|----:|-----|---|---|
| Oxff | Oxff | Oxff | ... |   0 |   0 |

PMU_DG_HP_POWERDOWN_TIMER Configures the wait cycles before powering down HP power domains. (R/W)

PMU_DG_HP_POWERUP_TIMER Configures the wait cycles before waking up HP power domains. (R/W)

PMU_DG_HP_PD_WAIT_TIMER Configures the wait cycles during sleep of HP power domains. (R/W)
```