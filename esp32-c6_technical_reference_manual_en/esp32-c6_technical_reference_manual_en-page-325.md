

```markdown
Register 8.8. PCR_I2C_SCLK_CONF_REG (0x0024)

PCR_I2C_SCLK_DIV_A Configures the denominator of the frequency divider factor for I2C function clock.
(R/W)

PCR_I2C_SCLK_DIV_B Configures the numerator of the frequency divider factor for I2C function clock.
(R/W)

PCR_I2C_SCLK_DIV_NUM Configures the integral part of the frequency divider factor for I2C function clock.
(R/W)

PCR_I2C_SCLK_SEL Configures to select clock source.
O (default): Select XTAL_CLK
1: Select RC_FAST_CLK
(R/W)

PCR_I2C_SCLK_EN Configures whether or not to enable I2C function clock.
O: Not enable
1: Enable
(R/W)
```