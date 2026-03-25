

```markdown
## Register 11.71. PMU_SLP_WAKEUP_CNTL1_REG (0x0128)

| 31 | 30 | [Reserved] | 0 |
|----:|----:|------------|---|
|    |    |            | Reset |

PMU_SLEEP_REJECT_ENA Configures the sleep rejection source. For the mapping between values and sources please refer to Table 11.4-1. (R/W)

PMU_SLP_REJECT_EN Configures whether to enable sleep rejection function.
0: Disable
1: Enable
(R/W)
```

```markdown
## Register 11.72. PMU_SLP_WAKEUP_CNTL2_REG (0x012C)

| 31 | [Reserved] | 0 |
|----:|------------|---|
|    |            | Reset |

PMU_WAKEUP_ENA Configures wake-up source. For the mapping between values and sources please refer to Table 11.4-1. (R/W)
```

```markdown
## Register 11.73. PMU_SLP_WAKEUP_CNTL3_REG (0x0130)

| 31 | [Reserved] | 18 | 17 | 16 | 15 | 8 | 7 | 0 |
|----:|------------|-----|-----|-----|-----|---|---|---|
|    |            |     |     |     |     |   |   | Reset |

PMU_LP_MIN_SLP_VAL Configures the LP_SLEEP sleep/wakeup wait time. (R/W)

PMU_HP_MIN_SLP_VAL Configures the HP_SLEEP sleep/wakeup wait time. (R/W)

PMU_SLEEP_PRT_SEL Configures to select the configuration data for sleep start and sleep end events. (R/W)
```