

```markdown
Register 45.2. APB_SARADC_APB_TSENS_CTRL2_REG (0x005C)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31-16     | (reserved)                                |                                                                             |
| 15        | APB_SARADC_TSENS_CLK_SEL                  | Configures the working clock for temperature sensor.<br>0: RC_FAST_CLK<br>1: XTAL_CLK<br>(R/W) |
| 14        | APB_SARADC_TSENS_CLK_INV                 | Configures the phase of the temperature sensor clock. (R/W)                   |
| 13-12     | APB_SARADC_TSENS_XPD_FORCE                | Configures whether to enable force power up/down the temperature sensor.<br>0: Disable force power up function<br>1: Disable force power down function<br>2: Enable force power up temperature sensor<br>3: Enable force power down temperature sensor (R/W) |
| 11-0      | APB_SARADC_TSENS_XPD_WAIT                 | Configure the wait time (in clock cycles) for the sensor to release from reset. (R/W) |
```