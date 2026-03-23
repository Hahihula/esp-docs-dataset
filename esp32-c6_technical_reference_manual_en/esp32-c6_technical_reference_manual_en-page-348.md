

```markdown
Register 8.45. PCR_SPI2_CONF_REG (0x0000)

PCR_SPI2_CLK_EN Configures whether or not to enable SPI2 APB clock.
O: Not enable
1: Enable
(R/W)

PCR_SPI2_RST_EN Configures whether or not to reset SPI2 module.
O: Not reset
1: Reset
(R/W)
```

```markdown
Register 8.46. PCR_SPI2_CLKM_CONF_REG (0x00C4)

PCR_SPI2_CLKM_SEL Configures to select clock source.
O (default): Select XTAL_CLK
1: Select PLL_F80M_CLK
2: Select RC_FAST_CLK
3: Reserved
(R/W)

PCR_SPI2_CLKM_EN Configures whether or not to enable SPI2 function clock.
O: Not enable
1: Enable
(R/W)
```