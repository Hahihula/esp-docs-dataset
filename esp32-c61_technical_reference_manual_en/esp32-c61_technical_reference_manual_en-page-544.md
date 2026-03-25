

```markdown
Register 11.32. PMU_HP_SLEEP_HP_CK_POWER_REG (0x007C)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 30  | PMU_HP_SLEEP_XPD_BBPLL_I2C     | Configures whether to enable BBPLL_I2C in HP_SLEEP state.                  |
| 29  | PMU_HP_SLEEP_XPD_BB_I2C        | Configures whether to enable BB_I2C in HP_SLEEP state.                     |
| 28  | PMU_HP_SLEEP_BBD                |                                                                             |
| 27  | (reserved)                     |                                                                             |
| 26  | PMU_HP_SLEEP_I2C_ISO_EN        | Configures whether to enable I2C_ISO in HP_SLEEP state.                    |
|     |                                 | O: Disable                                                                   |
|     |                                 | 1: Enable                                                                    |
|     |                                 | (R/W)                                                                        |

PMU_HP_SLEEP_XPD_BBPLL_I2C Configures whether to enable BBPLL_I2C in HP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_XPD_BB_I2C Configures whether to enable BB_I2C in HP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_XPD_BBPLL Configures whether to enable BBPLL in HP_SLEEP state.
O: Disable
1: Enable
(R/W)
```