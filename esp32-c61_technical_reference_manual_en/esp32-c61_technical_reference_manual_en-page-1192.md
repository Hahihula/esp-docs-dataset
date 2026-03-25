

```markdown
Register 32.2. APB_SARADC_APB_TSENS_CTRL2_REG (0x005C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 16  | APB_SARADC_TSENS_CLK_SEL                                                   |
| 15  | APB_SARADC_TSENS_CLK_INV                                                    |
| 14  | APB_SARADC_TSENS_XPD_FORCE                                                  |
| 13  | APB_SARADC_TSENS_XPD_WAIT                                                   |
| 12  |                                                                             |
| 0x0 | Reset                                                                       |

APB_SARADC_TSENS_CLK_SEL Configures the working clock for temperature sensor.
- 0: RC_FAST_CLK
- 1: XTAL_CLK
(R/W)

APB_SARADC_TSENS_CLK_INV Configures the phase of the temperature sensor clock. (R/W)

APB_SARADC_TSENS_XPD_FORCE Configures whether to enable force power up/down the temperature sensor.
- 0: Disable force power up function
- 1: Disable force power down function
- 2: Enable force power up temperature sensor
- 3: Enable force power down temperature sensor
(R/W)

APB_SARADC_TSENS_XPD_WAIT Configure the wait time (in clock cycles) for the senor to release from reset. (R/W)
```