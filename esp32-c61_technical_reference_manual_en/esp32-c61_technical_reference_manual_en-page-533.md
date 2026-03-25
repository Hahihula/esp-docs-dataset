

```markdown
Register 11.19. PMU_HP_MODEM_HP_CK_POWER_REG (0x0048)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 30  | PMU_HP_MODEM_XPD_BBPLL_I2C     | Configures whether to enable I2C_ISO in HP_MODEM state.                    |
| 29  | PMU_HP_MODEM_XPD_BBPLL_I2C     | O: Disable                                                                   |
| 28  | PMU_HP_MODEM_XPD_BB_I2C        | 1: Enable                                                                    |
| 27  | (reserved)                     |                                                                             |
| 26  | PMU_HP_MODEM_XPD_BB_I2C        | Configures whether to enable BB_I2C in HP_MODEM state.                      |
|     | O: Disable                     |                                                                                 |
|     | 1: Enable                      | (R/W)                                                                         |
|     |                                 |                                                                             |
|     | PMU_HP_MODEM_XPD_BBPLL_I2C     | Configures whether to enable BBPLL_I2C in HP_MODEM state.                  |
|     | O: Disable                     |                                                                                 |
|     | 1: Enable                      | (R/W)                                                                         |
|     |                                 |                                                                             |
|     | PMU_HP_MODEM_XPD_BBPLL         | Configures whether to enable BBPLL in HP_MODEM state.                       |
|     | O: Disable                     |                                                                                 |
|     | 1: Enable                      | (R/W)                                                                         |

Notice:
BB_I2C, BBPLL_I2C and XTAL must be turned on first before enabling BBPLL.
```