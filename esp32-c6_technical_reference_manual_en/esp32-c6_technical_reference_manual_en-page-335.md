

```markdown
Register 8.26. PCR_I2S_CONF_REG (0x006C)

PCR_I2S_CLK_EN Configures whether or not to enable I2S APB clock.
O: Not enable
1: Enable
(R/W)

PCR_I2S_RST_EN Configures whether or not to reset I2S module.
O: Not reset
1: Reset
(R/W)
```

```markdown
Register 8.27. PCR_I2S_TX_CLKM_CONF_REG (0x0070)

PCR_I2S_TX_CLKM_DIV_NUM Configures the integral part of I2S TX clock divider.
(R/W)

PCR_I2S_TX_CLKM_SEL Configures to select I2S TX module source clock.
O: Select XTAL_CLK
1: Select PLL_F240M_CLK
2: Select PLL_F160M_CLK
3: Select I2S_MCLK_in
(R/W)

PCR_I2S_TX_CLKM_EN Configures whether or not to enable I2S TX function clock.
O: Not enable
1: Enable
(R/W)
```