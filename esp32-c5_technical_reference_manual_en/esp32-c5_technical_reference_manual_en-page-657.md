

```markdown
Register 13.54. PMU_LP_CPU_PWRO_REG (0x0180)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             |                                                                             |
| 30  | PMU_LP_CPU_SLP_BYPASS_INTR_EN              | Configures whether to enable interrupt enable signal when LP CPU is in sleep mode.<br>0: Disable all interrupt signals to LP CPU<br>1: Enable interrupt signals to LP CPU (R/W) |
| 29  | PMU_LP_CPU_SLP_RESET_EN                    | Configures whether to reset LP CPU when it goes into sleep mode.<br>0: Do not reset<br>1: Reset (R/W) |
| 28  | PMU_LP_CPU_SLP_STALL_EN                    | Configures whether to stall LP CPU when it goes into sleep mode.<br>0: Do not stall<br>1: Stall (R/W) |
| 27  |                                             |                                                                             |
| 26  | PMU_LP_CPU_SLP_STALL_WAIT                  | Configures the time to wait for the stall to take effect after enabling stall state when the LP CPU enters sleep mode. The unit is LP_DYN_FAST_CLK. (R/W) |
| 25  |                                             |                                                                             |
| 24  |                                             |                                                                             |
| 23  |                                             |                                                                             |
| 22  |                                             |                                                                             |
| 21  |                                             |                                                                             |
| 20  |                                             |                                                                             |
| 19  |                                             | (reserved)                                                                   |
| 18  |                                             |                                                                             |
| 17  |                                             |                                                                             |
| 16  |                                             |                                                                             |
| 15  |                                             |                                                                             |
| 14  |                                             |                                                                             |
| 13  |                                             |                                                                             |
| 12  |                                             |                                                                             |
| 11  |                                             |                                                                             |
| 10  |                                             |                                                                             |
| 9   |                                             |                                                                             |
| 8   |                                             |                                                                             |
| 7   |                                             |                                                                             |
| 6   |                                             |                                                                             |
| 5   |                                             |                                                                             |
| 4   |                                             |                                                                             |
| 3   |                                             |                                                                             |
| 2   |                                             |                                                                             |
| 1   |                                             |                                                                             |
| 0   | Oxff                                       | Reset                                                                        |

PMU_LP_CPU_SLP_STALL_WAIT Configures the time to wait for the stall to take effect after enabling stall state when the LP CPU enters sleep mode. The unit is LP_DYN_FAST_CLK. (R/W)

PMU_LP_CPU_SLP_STALL_EN Configures whether to stall LP CPU when it goes into sleep mode.<br>0: Do not stall<br>1: Stall (R/W)

PMU_LP_CPU_SLP_RESET_EN Configures whether to reset LP CPU when it goes into sleep mode.<br>0: Do not reset<br>1: Reset (R/W)

PMU_LP_CPU_SLP_BYPASS_INTR_EN Configures whether to enable interrupt enable signal when LP CPU is in sleep mode.<br>0: Disable all interrupt signals to LP CPU<br>1: Enable interrupt signals to LP CPU (R/W)
```