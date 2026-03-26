

```markdown
Register 14.51. PMU_LP_CPU_PWR0_REG (0x0184)

Continued from the previous page...

PMU_LP_CPU_SLP_RESET_EN Configures whether to reset the LP CPU in sleep mode.
    0: Do not reset
    1: Reset
        (R/W)

PMU_LP_CPU_SLP_BYPASS_INTR_EN Configures whether to enable interrupt signals for the LP
CPU in sleep mode.
    0: Disable interrupt signals
    1: Enable interrupt signals
        (R/W)

Register 14.52. PMU_LP_CPU_PWR1_REG (0x0188)

PMU_LP_CPU_SLEEP_REQ Configures whether the LP CPU enters sleep.
    0: Does not enter sleep
    1: Enters sleep
        (WT)

Table 14.4-1 Wake-up Sources. (R/W)
```