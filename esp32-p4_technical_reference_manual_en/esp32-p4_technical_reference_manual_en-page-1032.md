

```markdown
Register 14.36. PMU_SLP_WAKEUP_CNTL2_REG (0x0128)

PMU_WAKEUP_ENA Configures wake-up source. For the mapping between values and sources please refer to Table 14.4-1. (R/W)


Register 14.37. PMU_SLP_WAKEUP_CNTL3_REG (0x012C)

PMU_LP_MIN_SLP_VAL Configures the minimum sleep time to enter LP_SLEEP. The unit is LP_DYN_SLOW_CLK. (R/W)

PMU_HP_MIN_SLP_VAL Configures the minimum sleep time to enter HP_SLEEP. The unit is LP_DYN_SLOW_CLK. (R/W)

PMU_SLEEP_PRT_SEL Configures the minimum sleep time mode.
0, 1, 3: Reserved
2: Protects both LP_SLEEP and HP_SLEEP simultaneously
(R/W)


Register 14.38. PMU_SLP_WAKEUP_CNTL4_REG (0x0130)

PMU_SLP_REJECT_CAUSE_CLR Write 1 to clear PMU_REJECT_CAUSE. (WT)
```