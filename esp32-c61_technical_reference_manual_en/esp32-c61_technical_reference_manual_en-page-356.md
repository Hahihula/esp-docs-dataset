

```markdown
Register 7.26. PCR_I2S_RX_CLKM_CONF_REG (0x006C)

PCR_I2S_RX_CLKM_DIV_NUM Configures the integral I2S clock divider value (R/W)

PCR_I2S_RX_CLKM_SEL Configures the clock source of I2S RX.
O (default): XTAL_CLK
1: PLL_F120M_CLK
2: PLL_F160M_CLK
3: I2S_MCLK_in
(R/W)

PCR_I2S_RX_CLKM_EN Configures whether or not to enable I2S RX functional clock.
O: Not enable
1: Enable
(R/W)

PCR_I2S_MCLK_SEL Configures to select master clock.
O (default): I2S_TX_CLK
1: I2S_RX_CLK
(R/W)
```