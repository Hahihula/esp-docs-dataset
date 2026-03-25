

```markdown
Register 11.50. PMU_IMM_HP_CK_POWER_REG (0x00CC)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | ... | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|-----|---|---|---|---|---|---|---|---|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

PMU_TIE_LOW_GLOBAL_BBPLL_ICG Configures whether to force disable the integrated clock gating (ICG) of PLL clock
O: No effect
1: Force disable
(WT)

PMU_TIE_LOW_GLOBAL_XTAL_ICG Configures whether to force disable the integrated clock gating (ICG) of XTAL clock.
O: No effect
1: Force disable
(WT)

PMU_TIE_LOW_I2C_RETENTION Configures whether to force the power-on reset (POR) signal for the analog I2C to low, releasing the reset.
O: No effect
1: Force disable
(WT)

PMU_TIE_LOW_XPD_BB_I2C Configures whether to force the power-on reset (POR) signal for BB_I2C to low, releasing the reset.
O: No effect
1: Force disable
(WT)

PMU_TIE_LOW_XPD_BBPLL_I2C Configures whether to force the power-on reset (POR) signal for BBPLL_I2C to low, releasing the reset.
O: No effect
1: Force disable
(WT)

PMU_TIE_LOW_XPD_BBPLL Configures whether to force the power-on reset (POR) signal for BB-PLL to low, releasing the reset.
O: No effect
1: Force disable
(WT)
```