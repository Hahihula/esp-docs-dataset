

```markdown
Register 7.29. PCR_I2S_RX_CLKM_CONF_REG (0x0078)

PCR_I2S_RX_CLKM_DIV_NUM Configures the integral divisor for I2S clock. (R/W)

PCR_I2S_RX_CLKM_SEL Configures the clock source of I2S RX.
O: XTAL_CLK
1: PLL_F96M_CLK
2: PLL_F64M_CLK
3: I2S_MCLK_in
(R/W)

PCR_I2S_RX_CLKM_EN Configures whether or not to enable I2S RX functional clock.
O: Not enable
1: Enable
(R/W)

PCR_I2S_MCLK_SEL Configures to select master clock.
O (default): I2S_RX_CLK
1: I2S_TX_CLK
(R/W)
```