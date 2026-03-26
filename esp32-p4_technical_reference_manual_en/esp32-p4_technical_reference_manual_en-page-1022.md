

```markdown
Register 14.23. PMU_HP_SLEEP_LP_CK_POWER_REG (0x00AC)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | ... | 0 |
|-----|----|----|----|----|----|----|-----|---|
|     | 0  | 1  | 0  | 0  | 0  | 0  | ... | 0 |

PMU_HP_SLEEP_XPD_LPPLL Configures whether to enable PLL_LP_CLK in HP_ACTIVE/HP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_XPD_XTAL32K Configures whether to enable XTAL32K_CLK in HP_ACTIVE/HP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_XPD_RC32K Configures whether to enable RC32K_CLK in HP_ACTIVE/HP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_XPD_FOSC_CLK Configures whether to enable RC_FAST_CLK in HP_ACTIVE/HP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_PD_OSC_CLK Configures whether to enable RC_SLOW_CLK in HP_ACTIVE/HP_SLEEP state.
O: Disable
1: Enable
(R/W)
```