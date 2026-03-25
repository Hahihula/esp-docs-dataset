

```markdown
Register 11.21. PMU_HP_SLEEP_LP_DIG_POWER_REG (0x00A8)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | ... | 0 |
|-----|----|----|----|----|----|----|-----|---|
|     |    |    |    |    |    |    | (reserved) | Reset |

PMU_HP_SLEEP_BOD_SOURCE_SEL Configures whether to enable brown-out detection in HP_SLEEP.(R/W)

PMU_HP_SLEEP_VDDBAT_MODE Selects the source of VDD_RTC.
0: VDDA_PMU
1: VBAT
2,3: reserved
(R/W)

PMU_HP_SLEEP_LP_MEM_DSLP Configures whether to enable Memory Deep-sleep mode for the 4 KB SRAM in HP_ACTIVE/HP_SLEEP state.
0: Disable
1: Enable
(R/W)
```