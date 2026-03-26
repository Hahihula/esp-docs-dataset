

```markdown
Register 14.28. PMU_IMM_HP_CK_POWER_REG (0x00CC)

| 31 | 30 | 27 | 26 | 23 | 22 | 21 | 20 | 17 | 16 | 15 | 14 | 11 | 10 | 7 | 6 | 5 | 4 | Reset |
|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|------|
|   O |   O |   O |   O |   O |   O |   O |   O |   O |   O |   O |   O |   O |   O |   O |   O |   O |   O | Reset |

PMU_TIE_LOW_GLOBAL_PLL_ICG Configures whether to power down global PLL clock gating bitmap.
O: No effect
1: Power down
(WT)

PMU_TIE_LOW_GLOBAL_XTAL_ICG Configures whether to power down XTAL clock.
O: No effect
1: Power down
(WT)

PMU_TIE_LOW_I2C_RETENTION Configures whether to power down ANALOG I2C retention.
O: No effect
1: Power down
(WT)

PMU_TIE_LOW_XPD_PLL_I2C Configures whether to power down global PLL I2C clock power bitmap.
O: No effect
1: Power down
(WT)

PMU_TIE_LOW_XPD_PLL Configures whether to power down global PLL clock power bitmap.
O: No effect
1: Power down
(WT)

PMU_TIE_LOW_XPD_XTAL Configures whether to power down XTAL clock power.
O: No effect
1: Power down
(WT)

PMU_TIE_HIGH_GLOBAL_PLL_ICG Configures whether to enable PLL clock gating bitmap.
O: No effect
1: Enable
(WT)
```