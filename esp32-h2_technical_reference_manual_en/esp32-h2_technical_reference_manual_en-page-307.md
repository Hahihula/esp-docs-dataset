

```markdown
Register 7.31. PCR_SARADC_CONF_REG (0x0080)
```

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 4   | PCR_SARADC_REG_RST_EN          | Configures whether or not to reset APB registers of SAR ADC.                |
|     | O: Not reset                   |                                                                                 |
|     | 1: Reset                       | (R/W)                                                                        |
| 3   | PCR_SARADC_CLK_EN              | Configures whether or not to enable APB_CLK for SAR ADC.                    |
|     | O: Not enable                  |                                                                                 |
|     | 1: Enable                      | (R/W)                                                                        |
| 2   | PCR_SARADC_RST_EN              | Configures whether or not to reset functional registers of SAR ADC.          |
|     | O: Not reset                   |                                                                                 |
|     | 1: Reset                       | (R/W)                                                                        |
```