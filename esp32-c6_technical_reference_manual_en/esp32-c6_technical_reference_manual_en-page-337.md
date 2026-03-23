

```markdown
Chapter 8 Reset and Clock

Register 8.29. PCR_I2S_RX_CLKM_CONF_REG (0x0078)

PCR_I2S_RX_CLKM_DIV_NUM Configures the integral part of I2S clock divider value.
(R/W)

PCR_I2S_RX_CLKM_SEL Configures to select I2S RX module source clock.
O: Not select any clock
1: Select PLL_F240M_CLK
2: Select PLL_F160M_CLK
3: Select I2S_MCLK_in
(R/W)

PCR_I2S_RX_CLKM_EN Configures whether or not to enable I2S RX function clock.
O: Not enable
1: Enable
(R/W)

PCR_I2S_MCLK_SEL Configures to select master clock.
O (default): Select I2S_RX_CLK
1: Select I2S_TX_CLK
(R/W)
```