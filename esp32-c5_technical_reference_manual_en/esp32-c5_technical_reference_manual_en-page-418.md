

```markdown
Register 9.29. PCR_I2S_TX_CLKM_CONF_REG (0x0078)

PCR_I2S_TX_CLKM_DIV_NUM Configures the integral part of I2S TX clock divisor.
(R/W)

PCR_I2S_TX_CLKM_SEL Configures the clock source of I2S TX.
O: XTAL_CLK
1: PLL_F240M_CLK
2: PLL_F160M_CLK
3: I2S_MCLK_in
(R/W)

PCR_I2S_TX_CLKM_EN Configures whether or not to enable I2S TX functional clock.
O: Not enable
1: Enable
(R/W)
```