

```markdown
Register 23.6. LP_ANA_INT_ST_REG (0x0024)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | ... | 0 |
|-----|----:|----:|----:|----:|----:|----:|-----|---|
|     |    |    |    |    |    |    | (reserved) | Reset |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | ... | 0 |

LP_ANA_VDDBAT_CHARGE_UPVOLTAGE_INT_ST The interrupt is triggered and sent to CPU when the voltage of VDD_BAT increases to the charging threshold. (RO)

LP_ANA_VDDBAT_CHARGE_UNDERVEROLTAGE_INT_ST The interrupt is triggered and sent to CPU when the voltage of VDD_BAT decreases to the charging threshold. (RO)

LP_ANA_VDDBAT_UPVOLTAGE_INT_ST The interrupt is triggered and sent to CPU when the voltage of VDD_BAT increases to the brown-out threshold. (RO)

LP_ANA_VDDBAT_UNDERVEROLTAGE_INT_ST The interrupt is triggered and sent to CPU when the voltage of VDD_BAT decreases to the brown-out threshold. (RO)

LP_ANA_BOD_MODEO_INT_ST The brown-out interrupt in Mode O is triggered and sent to CPU. (RO)
```