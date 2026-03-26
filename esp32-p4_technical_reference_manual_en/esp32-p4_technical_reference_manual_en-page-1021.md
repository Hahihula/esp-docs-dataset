

```markdown
Register 14.22. PMU_HP_SLEEP_LP_DIG_POWER_REG (0x00A8)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | ... | 0 |
|-----|----|----|----|----|----|----|----|-----|---|
|     |    |    |    |    |    |    |    | (reserved) | Reset |

PMU_HP_SLEEP_PD_LP_PERI_PD_EN
HP_ACTIVE/HP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_BOD_SOURCE_SEL
Configures whether to enable brown-out detection in HP_ACTIVE/HP_SLEEP. (R/W)

PMU_HP_SLEEP_VDBAT_MODE
Configures whether to enable VBAT power in HP_ACTIVE/HP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_LP_MEM_DSLP
Configures whether to enable Memory Deep-sleep mode for the LP SRAM in HP_ACTIVE/HP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_PD_LP_PERI_PD_EN
Configures whether to power down LP PD Peripherals in HP_ACTIVE/HP_SLEEP state.
O: Power up
1: Power down
(R/W)
```