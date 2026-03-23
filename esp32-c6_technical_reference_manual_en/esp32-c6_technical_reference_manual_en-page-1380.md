

```markdown
Register 39.18. APB_SARADC_TSENS_CTRL2_REG (0x005C)

APB_SARADC_TSENS_CLK_SEL   Configures the working clock for temperature sensor.
    0: RC_FAST_CLK
    1: XTAL_CLK
    (R/W)

APB_SARADC_TSENS_CLK_INV   Configures the phase of sensor sample clock. (R/W)

APB_SARADC_TSENS_XPD_FORCE   Configures whether to enable force power up/down the temperature sensor.
    0/1: Disable force power up/down function
    2: Enable force power up temperature sensor
    3: Enable force power down temperature sensor
    (R/W)

APB_SARADC_TSENS_XPD_WAIT   Configure the wait time for analog circuit build up. (R/W)
```

```markdown
Register 39.19. APB_SARADC_CALI_REG (0x0060)

APB_SARADC_CALI_CFG   Configures the SAR ADC calibration factor. (R/W)
```