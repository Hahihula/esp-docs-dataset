

```markdown
Register 11.22. PMU_HP_SLEEP_LP_CK_POWER_REG (0x00AC)

| Bit | 31 | 30 | 29 | 28 | 27 | ... | 0 |
|-----|----|----|----|----|----|-----|---|
|     |    |    | PMU_HP_SLEEP_XPD_FOSC_CLK (reserved) | PMU_HP_SLEEP_XPD_XTAL32K (reserved) | ... | Reset |

PMU_HP_SLEEP_XPD_XTAL32K Configures whether to power up XTAL32K_CLK analog part circuit in HP_ACTIVE/HP_SLEEP state.
- O: Power down
- 1: Power up
(R/W)

PMU_HP_SLEEP_XPD_FOSC_CLK Configures whether to power up RC_FAST_CLK analog part circuit in HP_ACTIVE/HP_SLEEP state.
- O: Power down
- 1: Power up
(R/W)

Register 11.23. PMU_LP_SLEEP_XTAL_REG (0x00BC)

| Bit | 31 | 30 |
|-----|----|----|
|     |    | PMU_LP_SLEEP_XPD_XTAL |

PMU_LP_SLEEP_XPD_XTAL Configures whether to enable XTAL_CLK analog source in LP_SLEEP state.
- O: Disable
- 1: Enable
(R/W)
```