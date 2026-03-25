

```markdown
## Register 11.74. PMU_SLP_WAKEUP_CNTL4_REG (0x0134)

| 31 | 30 | ... | 0 |
|----:|----:|-----|---|
|   0 |   0 | all zeros | Reset |

**PMU_SLP_REJECT_CAUSE_CLR** Write 1 to clear PMU_REJECT_CAUSE. (WT)

## Register 11.75. PMU_SLP_WAKEUP_CNTL5_REG (0x0138)

| 31 | 24 | 23 | 22 | 21 | 20 | ... | 0 |
|----:|----:|----:|----:|----:|----:|-----|---|
|   1 |   0 |   0 |   0 |   0 | 128 | all zeros | Reset |

**PMU_MODEM_WAIT_TARGET** Configures the wait timer after the Modem wakeup. (R/W)

**PMU_LP_ANA_WAIT_TARGET** Configures the wait timer after turning on the analog power. (R/W)

## Register 11.76. PMU_SLP_WAKEUP_CNTL6_REG (0x013C)

| 31 | 30 | ... | 20 | 19 |
|----:|----:|-----|----:|----:|
|   0 |   0 | all zeros |    0 | 128 |

**PMU_SOC_WAKEUP_WAIT** Configures the HP_MODEM wakeup wait timer. (R/W)

**PMU_SOC_WAKEUP_WAIT_CFG** Configures to select the wait timer for HP_MODEM wakeup. (R/W)
```