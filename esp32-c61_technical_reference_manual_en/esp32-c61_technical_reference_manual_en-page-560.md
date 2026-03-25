

```markdown
Chapter 11 Low-Power Management

Register 11.50. PMU_IMM_HP_CK_POWER_REG (0x00CC)

Continued from the previous page...

PMU_TIE_HIGH_XPD_XTAL Configures whether to force the power-on reset (POR) signal for XTAL_CLK to high, putting it into reset.
O: No effect
1: Force enable
(WT)

Register 11.51. PMU_IMM_SLEEP_SYSCLK_REG (0x00D0)


PMU_UPDATE_DIG_ICG_SWITCH Configures whether to force power up XTAL.
O: No effect
1: Force enable
(WT)

PMU_TIE_LOW_ICG_SLP_SEL Configures whether to force disable the integrated clock gating (ICG) of PMU clock controller.
O: No effect
1: Force disable
(WT)

PMU_TIE_HIGH_ICG_SLP_SEL Configures whether to force enable the integrated clock gating (ICG) of PMU clock controller.
O: No effect
1: Force enable
(WT)

PMU_UPDATE_DIG_SYS_CLK_SEL Configures whether to force update the HP_ROOT_CLK configuration stored in PMU registers.
O: No effect
1: Force update
(WT)
```