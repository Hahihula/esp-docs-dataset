

```markdown
Register 14.15. PMU_HP_SLEEP_BIAS_REG (0x0080)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | Reset |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|------|
|     |    |    |    |    | (reserved) | PMU_HP_SLEEP_DCM_MODE | PMU_HP_SLEEP_DCM_VSET | 0 | 0 | 0 | 0 | 0 | 0 | 0 |      |

PMU_HP_SLEEP_DCM_VSET Regulates the DCDC voltage in HP_SLEEP state. (R/W)

PMU_HP_SLEEP_DCM_MODE Configures whether to enable DCDC status in HP_SLEEP state.
    0: Disable
    1: Enable
    2, 3: Reserved
(R/W)
```