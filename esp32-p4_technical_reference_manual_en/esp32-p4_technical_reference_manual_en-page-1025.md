

```markdown
Register 14.27. PMU_LP_SLEEP_LP_CK_POWER_REG (0x00C4)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | ... | 0 |
|-----|----|----|----|----|----|----|-----|---|
|     |    | PMU_LP_SLEEP_PD_OSC_CLK | PMU_LP_SLEEP_XPD_FOSC_CLK | PMU_LP_SLEEP_XPD_RC32K | PMU_LP_SLEEP_XPD_XTAL32K | PMU_LP_SLEEP_XPD_LPLL | (reserved) |
| Reset | 0 | 1 | 0 | 0 | 0 | 0 | ... | 0 |

PMU_LP_SLEEP_XPD_LPLL Configures whether to enable PLL_LP_CLK in LP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_LP_SLEEP_XPD_XTAL32K Configures whether to enable XTAL32K_CLK in LP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_LP_SLEEP_XPD_RC32K Configures whether to enable RC32K_CLK in LP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_LP_SLEEP_XPD_FOSC_CLK Configures whether to enable RC_FAST_CLK in LP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_LP_SLEEP_PD_OSC_CLK Configures whether to enable RC_SLOW_CLK in LP_SLEEP state.
O: Disable
1: Enable
(R/W)
```