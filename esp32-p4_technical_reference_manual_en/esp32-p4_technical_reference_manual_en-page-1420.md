
```markdown
Register 23.5. LP_ANA_INT_RAW_REG (0x0020)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | ... | 0 |
|-----|----|----|----|----|----|----|-----|---|
|     | LP_ANA_BOD_MODEO_INT_RAW | LP_ANA_VDDBAT_LUNDERVOLTAGE_INT_RAW | LP_ANA_VDDBAT_CHARGE_UPVOLTAGE_INT_RAW | (reserved) | Reset |
```


LP_ANA_VDDBAT_CHARGE_UPVOLTAGE_INT_RAW  The interrupt is triggered when the voltage of VDD_BAT increases to the charging threshold. (RO)

LP_ANA_VDDBAT_CHARGE_UNDERVERLTAGE_INT_RAW  The interrupt is triggered when the voltage of VDD_BAT decreases to the charging threshold. (RO)

LP_ANA_VDDBAT_UPVOLTAGE_INT_RAW  The interrupt is triggered when the voltage of VDD_BAT increases to the brown-out threshold. (RO)

LP_ANA_VDDBAT_UNDERVERLTAGE_INT_RAW  The interrupt is triggered when the voltage of VDD_BAT decreases to the brown-out threshold. (RO)

LP_ANA_BOD_MODEO_INT_RAW  Brown-out interrupt in Mode 0. (RO)
```