

```markdown
Chapter 11 Low-Power Management

Register 11.50. PMU_IMM_HP_CK_POWER_REG (0x00CC)

Continued from the previous page...

PMU_TIE_LOW_XPD_XTAL Configures whether to force the power-on reset (POR) signal for XTAL_CLK to low, releasing the reset.
O: No effect
1: Force disable
(WT)

PMU_TIE_HIGH_GLOBAL_BBPLL_ICG Configures whether to force enable the integrated clock gating (ICG) of PLL clock.
O: No effect
1: Force enable
(WT)

PMU_TIE_HIGH_GLOBAL_XTAL_ICG Configures whether to force enable the integrated clock gating (ICG) of XTAL clock.
O: No effect
1: Force enable
(WT)

PMU_TIE_HIGH_I2C_RETENTION Configures whether to force the power-on reset (POR) signal for the analog I2C to high, putting it into reset.
O: No effect
1: Force enable
(WT)

PMU_TIE_HIGH_XPD_BB_I2C Configures whether to force the power-on reset (POR) signal for BB_I2C to high, putting it into reset.
O: No effect
1: Force enable
(WT)

PMU_TIE_HIGH_XPD_BBPLL_I2C Configures whether to force the power-on reset (POR) signal for BBPLL_I2C to high, putting it into reset.
O: No effect
1: Force enable
(WT)

PMU_TIE_HIGH_XPD_BBPLL Configures whether to force the power-on reset (POR) signal for BB-PLL to high, putting it into reset.
O: No effect
1: Force enable
(WT)

Continued on the next page...
```