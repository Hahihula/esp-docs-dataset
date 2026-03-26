

```markdown
Register 23.7. LP_ANA_INT_ENA_REG (0x0028)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | ... | 0 |
|-----|----|----|----|----|----|----|-----|---|
|     | LP_ANA_BOD_MODEO_INT_ENA | LP_ANA_VDDBAT_UNDERVOLTAGE_INT_ENA | LP_ANA_VDDBAT_CHARGE_UPVOLTAGE_INT_ENA | (reserved) |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | ... | Reset |

LP_ANA_VDDBAT_CHARGE_UPVOLTAGE_INT_ENA Configure whether to enable the interrupt which is triggered when the voltage of VDD_BAT increases to the charging threshold.
- O: No
- 1: Yes
(R/W)

LP_ANA_VDDBAT_CHARGE_UNDERVOLTAGE_INT_ENA Configures whether to enable the interrupt which is triggered when the voltage of VDD_BAT reduces to the charging threshold.
- O: Yes
- 1: No
(R/W)

LP_ANA_VDDBAT_UPVOLTAGE_INT_ENA Configures whether to enable the interrupt which is triggered when the voltage of VDD_BAT increases to the brown-out threshold.
- O: Yes
- 1: No
(R/W)

LP_ANA_VDDBAT_UNDERVOLTAGE_INT_ENA Configures whether to enable the interrupt which is triggered when the voltage of VDD_BAT reduces to the brown-out threshold.
- O: No
- 1: Yes
(R/W)

LP_ANA_BOD_MODEO_INT_ENA Configures whether to enable the brown-out interrupt in Mode 0.
- O: No
- 1: Yes
(R/W)
```