

```markdown
Register 39.2. APB_SARADC_APB_TSENS_CTRL2_REG (0x005C)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                            |                                                                             |
| 16  | APB_SARADC_TSENS_CLK_SEL                   | Configures the working clock for temperature sensor.                         |
|     | O: RC_FAST_CLK                             |                                                                                 |
|     | 1: XTAL_CLK                                | (R/W)                                                                        |
| 15  | APB_SARADC_TSENS_CLK_INV                   | Configures the phase of the temperature sensor clock. (R/W)                  |
| 14  | APB_SARADC_TSENS_XPD_FORCE                 | Configures whether to enable force power up/down the temperature sensor.      |
|     | O: Disable force power up function         |                                                                                 |
|     | 1: Disable force power down function       |                                                                                 |
|     | 2: Enable force power up temperature sensor |                                                                                 |
|     | 3: Enable force power down temperature sensor | (R/W)                                                                        |
| 13  | APB_SARADC_TSENS_XPD_WAIT                  | Configure the wait time (in clock cycles) for the senor to release from reset. (R/W) |
```