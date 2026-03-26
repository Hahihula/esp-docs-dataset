

```markdown
Register 10.74. LPPERI_RESET_EN_REG (0x0008)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | LPPERI_RST_EN_LP_CORE | LPPERI_RST_EN_LP_ROM | LPPERI_RST_EN_LP_INTR | LPPERI_RST_EN_LP_I2C | LPPERI_RST_EN_LP_LUART | LPPERI_RST_EN_LP_ADC | LPPERI_RST_EN_LP_SPL | LPPERI_RST_EN_LP_TOUCH | LPPERI_RST_EN_LP_IOMUX | LPPERI_RST_EN_LP_EFUSE | LPPERI_RST_EN_LP_PMS | LPPERI_RST_EN_LP_TSENS | (reserved) |
|     | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

LPPERI_RST_EN_LP_TSENS Configures whether to reset LP temperature sensor.
- 0: Release from reset
- 1: Reset (R/W)

LPPERI_RST_EN_LP_PMS Configures whether to reset LP PMS.
- 0: Release from reset
- 1: Reset (R/W)

LPPERI_RST_EN_LP_EFUSE Configures whether to reset LP eFuse.
- 0: Release from reset
- 1: Reset (R/W)

LPPERI_RST_EN_LP_IOMUX Configures whether to reset LP IO MUX.
- 0: Release from reset
- 1: Reset (R/W)

LPPERI_RST_EN_LP_TOUCH Configures whether to reset LP touch sensor.
- 0: Release from reset
- 1: Reset (R/W)

LPPERI_RST_EN_LP_SPL Configures whether to reset LP SPI.
- 0: Release from reset
- 1: Reset (R/W)

LPPERI_RST_EN_LP_ADC Configures whether to reset LP ADC.
- 0: Release from reset
- 1: Reset (R/W)
```