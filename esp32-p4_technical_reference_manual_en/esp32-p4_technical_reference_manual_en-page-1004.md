

```markdown
Register 14.4. PMU_HP_ACTIVE_HP_CK_POWER_REG (0x0014)

| Bit | 31 | 30 | 27 | 26 | 23 | 22 | 21 | 20 |
|-----|----|----|----|----|----|----|----|----|
|     | (reserved) | PMU_HP_ACTIVE_XPD_PLL | PMU_HP_ACTIVE_XPD_PLL_I2C | PMU_HP_ACTIVE_I2C_RETENTION | PMU_HP_ACTIVE_I2C_ISO_EN | (reserved) |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

PMU_HP_ACTIVE_I2C_ISO_EN   Configure whether to power up ANALOG_I2C in HP_ACTIVE state.
- 0: Power down
- 1: Power up
(R/W)

PMU_HP_ACTIVE_I2C_RETENTION Configures whether to enable ANALOG_I2C retention status in HP_ACTIVE state.
- 0: Disable
- 1: Enable
(R/W)

PMU_HP_ACTIVE_XPD_PLL_I2C   Configures whether to enable PLL I2C controllers in HP_ACTIVE state. Each bit controls a PLL I2C register group.
- 0: Disable
- 1: Enable
(R/W)

PMU_HP_ACTIVE_XPD_PLL       Configures whether to enable the analog power domains in HP system in HP_ACTIVE state. Bit 0 controls CPLL_CLK, bit 1 controls SPLL_CLK, bit 2 controls Audio PLL, bit 3 controls SDIO PLL.
- 0: Disable
- 1: Enable
(R/W)
```