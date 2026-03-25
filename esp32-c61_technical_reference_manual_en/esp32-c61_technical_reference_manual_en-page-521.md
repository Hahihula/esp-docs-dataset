

```markdown
Register 11.6. PMU_HP_ACTIVE_HP_CK_POWER_REG (0x0014)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | ... | 0 |
|-----|----|----|----|----|----|----|----|-----|---|
|     |    | (reserved) | PMU_HP_ACTIVE_XPD_BBPLL_I2C | PMU_HP_ACTIVE_XPD_BB_I2C | PMU_HP_ACTIVE_I2C_ISO_EN | ... | Reset |

PMU_HP_ACTIVE_I2C_ISO_EN Configures whether to enable I2C_ISO in HP_ACTIVE state.
- 0: Disable
- 1: Enable
(R/W)

PMU_HP_ACTIVE_XPD_BB_I2C Configures whether to enable BB_I2C in HP_ACTIVE state.
- 0: Disable
- 1: Enable
(R/W)

PMU_HP_ACTIVE_XPD_BBPLL_I2C Configures whether to enable BBPLL_I2C in HP_ACTIVE state.
- 0: Disable
- 1: Enable
(R/W)

PMU_HP_ACTIVE_XPD_BBPLL Configures whether to enable BBPLL in HP_ACTIVE state.
- 0: Disable
- 1: Enable
(R/W)

Notice:
BB_I2C, BBPLL_I2C and XTAL must be turned on first before enabling BBPLL.
```