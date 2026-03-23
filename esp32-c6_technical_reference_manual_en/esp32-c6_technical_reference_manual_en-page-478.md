

```markdown
Register 12.53. PMU_LP_CPU_PWRO_REG (0x017C)
```

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             |                                                                             |
| 30  | PMU_LP_CPU_SLP_BYPASS_INTR_EN              | Configures whether to enable interrupt enable signal when LP CPU is in sleep mode. <br> O: Disable all interrupt signals to LP CPU <br> 1: Enable interrupt signals to LP CPU (R/W) |
| 29  | PMU_LP_CPU_SLP_RESET_EN                    | Configures whether to reset LP CPU when it goes into sleep mode. <br> O: Do not reset <br> 1: Reset (R/W) |
| 28  | PMU_LP_CPU_SLP_STALL_EN                    | Configures whether to stall LP CPU when it goes into sleep mode. <br> O: Do not stall <br> 1: Stall (R/W) |
| 27  |                                             |                                                                             |
| 26  | PMU_LP_CPU_SLP_STALL_WAIT                  | Configures the time to wait for the stall to take effect after enabling stall state when the LP CPU enters sleep mode. The unit is LP_DYN_FAST_CLK. (R/W) |
|     |                                             |                                                                             |
| 0   | Reset                                      | All bits reset to 0x00 except PMU_LP_CPU_SLP_STALL_EN which resets to 0. |

```markdown
PMU_LP_CPU_SLP_STALL_WAIT Configures the time to wait for the stall to take effect after enabling stall state when the LP CPU enters sleep mode. The unit is LP_DYN_FAST_CLK. (R/W)

PMU_LP_CPU_SLP_STALL_EN Configures whether to stall LP CPU when it goes into sleep mode.
O: Do not stall
1: Stall
(R/W)

PMU_LP_CPU_SLP_RESET_EN Configures whether to reset LP CPU when it goes into sleep mode.
O: Do not reset
1: Reset
(R/W)

PMU_LP_CPU_SLP_BYPASS_INTR_EN Configures whether to enable interrupt enable signal when LP CPU is in sleep mode.
O: Disable all interrupt signals to LP CPU
1: Enable interrupt signals to LP CPU
(R/W)
```