

```markdown
Register 14.51. PMU_LP_CPU_PWR0_REG (0x0184)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             |                                                                             |
| 30  | PMU_LP_CPU_SLP_WAITI_RDY                   | Indicates whether the LP CPU is in the waiti state.                          |
|     | O: Does not enter the state                |                                                                                 |
|     | 1: Enters the state                        | (RO)                                                                         |
| 29  | PMU_LP_CPU_STALL_RDY                       | Indicates whether the LP CPU is in the stall state.                          |
|     | O: Does not enter the state                |                                                                                 |
|     | 1: Enters the state                        | (RO)                                                                         |
| 28  | PMU_LP_CPU_FORCE_STALL                     | Configures the LP CPU to enter the stall state.                             |
|     | O: Does not enter the state                |                                                                                 |
|     | 1: Enters the state                        | (R/W)                                                                        |
| 27  | PMU_LP_CPU_SLP_WAITI_FLAG_EN               | Configures whether the LP CPU needs to enter the waiti state when entering sleep mode. |
|     | O: Does not enter the state                |                                                                                 |
|     | 1: Enters the state                        | (R/W)                                                                        |
| 26  | PMU_LP_CPU_SLP_STALL_FLAG_EN               | Configures whether the LP CPU needs to enter the stall state when entering sleep mode. |
|     | O: Does not enter the state                |                                                                                 |
|     | 1: Enters the state                        | (R/W)                                                                        |
| 25  | PMU_LP_CPU_SLP_STALL_WAIT                  | Configures the time to wait for the stall to take effect after enabling stall state when the LP CPU enters sleep mode. The unit is LP_DYN_FAST_CLK. (R/W) |
|     |                                             |                                                                             |
| 24  | PMU_LP_CPU_SLP_STALL_EN                    | Configures whether to pause the LP CPU in sleep mode.                        |
|     | O: Do not pause                            |                                                                                 |
|     | 1: Pause                                   | (R/W)                                                                        |

Continued on the next page...
```