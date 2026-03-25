

```markdown
Register 13.37. PMU_LP_SLEEP_LP_CK_POWER_REG (0x00C4)
```

| Bit | 31 | 30 | 29 | 28 | 27 | ... | 0 |
|-----|----|----|----|----|----|-----|---|
|     | (reserved) | PMU_LP_SLEEP_XPD_FOSC_CLK | (reserved) | PMU_LP_SLEEP_XPD_XTAL32K | ... | Reset |

PMU_LP_SLEEP_XPD_XTAL32K Configures whether to power up XTAL32K_CLK analog part circuit in LP_SLEEP state.
- 0: Power down
- 1: Power up
(R/W)

PMU_LP_SLEEP_XPD_FOSC_CLK Configures whether to power up RC_FAST_CLK analog part circuit in LP_SLEEP state.
- 0: Power down
- 1: Power up
(R/W)
```