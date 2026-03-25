

```markdown
Register 11.58. PMU_POWER_WAIT_TIMER1_REG (0x00F0)

| 31 | 23 | 22 | 16 | 15 | 9 | 8 | 7 | 0 |
|----:|----:|----:|----:|----:|---:|---:|---:|---:|
| Oxff |     |     | 0x3f | 0x3f | 0 | 0 | 0 | Reset |

PMU_DG_LP_POWERDOWN_TIMER Configures the wait cycles before powering down LP power domains. (R/W)

PMU_DG_LP_POWERUP_TIMER Configures the wait cycles before waking up LP power domains. (R/W)

PMU_DG_LP_PD_WAIT_TIMER Configures the wait cycles during sleep of LP power domains. (R/W)
```

```markdown
Register 11.59. PMU_POWER_WAIT_TIMER2_REG (0x00F4)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|----:|----:|----:|----:|----:|---:|---:|---:|
| Oxff |     |     | 0xff | 0xff | 0xff | Reset |

PMU_DG_LP_ISO_WAIT_TIMER Configures the wait cycles of LP ISO control. (R/W)

PMU_DG_LP_RST_WAIT_TIMER Configures the wait cycles of LP reset control. (R/W)

PMU_DG_HP_ISO_WAIT_TIMER Configures the wait cycles of HP ISO control. (R/W)

PMU_DG_HP_RST_WAIT_TIMER Configures the wait cycles of HP reset control. (R/W)
```