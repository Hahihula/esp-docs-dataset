

```markdown
Register 14.14. PMU_HP_SLEEP_HP_CK_POWER_REG (0x007C)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | PMU_HP_SLEEP_XPD_PLL                       | Configures whether to enable PLL I2C controllers in HP_SLEEP state. Each bit controls a PLL I2C register group.<br>0: Disable<br>1: Enable (R/W) |
| 27  | PMU_HP_SLEEP_I2C_RETENTION                 | Configures whether to enable ANALOG_I2C retention status in HP_SLEEP state.<br>0: Disable<br>1: Enable (R/W) |
| 26  | PMU_HP_SLEEP_I2C_ISO_EN                    | Configure whether to power up ANALOG_I2C in HP_SLEEP state.<br>0: Power down<br>1: Power up (R/W) |
| 23  | PMU_HP_SLEEP_XPD_PLL_I2C                   | Configures whether to enable the analog power domains in HP system in HP_SLEEP state. Bit 0 controls CPLL_CLK, bit 1 controls SPLL_CLK, bit 2 controls Audio PLL, bit 3 controls SDIO PLL.<br>0: Disable<br>1: Enable (R/W) |
| 22-20 | (reserved)                               |                                                                             |
| 20  | PMU_HP_SLEEP_I2C_ISO_EN                    |                                                                             |
| 19  | PMU_HP_SLEEP_XPD_PLL                       |                                                                             |
| 18  | PMU_HP_SLEEP_I2C_RETENTION                 |                                                                             |
| 17-0| (reserved)                                 |                                                                             |

PMU_HP_SLEEP_I2C_ISO_EN Configure whether to power up ANALOG_I2C in HP_SLEEP state.
O: Power down
1: Power up
(R/W)

PMU_HP_SLEEP_I2C_RETENTION Configures whether to enable ANALOG_I2C retention status in HP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_XPD_PLL_I2C Configures whether to enable PLL I2C controllers in HP_SLEEP state. Each bit controls a PLL I2C register group.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_XPD_PLL Configures whether to enable the analog power domains in HP system in HP_SLEEP state. Bit 0 controls CPLL_CLK, bit 1 controls SPLL_CLK, bit 2 controls Audio PLL, bit 3 controls SDIO PLL.
O: Disable
1: Enable
(R/W)
```