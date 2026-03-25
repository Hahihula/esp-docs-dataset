

```markdown
## Register 9.46. PCR_SPI2_CONF_REG (0x00C4)

PCR_SPI2_CLK_EN Configures whether or not to enable APB_CLK for SPI2.
- O: Not enable
- 1: Enable
(R/W)

PCR_SPI2_RST_EN Configures whether or not to reset SPI2.
- O: Not reset
- 1: Reset
(R/W)

PCR_SPI2_READY Represents whether or not SPI2 is released from reset.
- O: Not released
- 1: Released
(RO)
```

```markdown
## Register 9.47. PCR_SPI2_CLKM_CONF_REG (0x00C8)

PCR_SPI2_CLKM_SEL Configures the clock source of SPI2.
- O (default): XTAL_CLK
- 1: PLL_F160M_CLK
- 2: RC_FAST_CLK
- 3: PLL_F120M_CLK
(R/W)

PCR_SPI2_CLKM_EN Configures whether or not to enable SPI2 functional clock.
- O: Not enable
- 1: Enable
(R/W)
```