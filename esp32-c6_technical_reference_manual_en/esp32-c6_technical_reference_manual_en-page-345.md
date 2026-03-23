

```markdown
Chapter 8 Reset and Clock

Register 8.41. PCR_PARL_CLK_RX_CONF_REG (0x00A8)

PCR_PARL_CLK_RX_DIV_NUM Configures the integral part of the frequency divider factor for PARL RX clock.
(R/W)

PCR_PARL_CLK_RX_SEL Configures to select clock source.

O (default): Select XTAL
1: Select PLL_F240M_CLK
2: Select RC_FAST_CLK
3: Use the clock from chip pin
(R/W)

PCR_PARL_CLK_RX_EN Configures whether or not to enable PARL RX clock.
O: Not enable
1: Enable
(R/W)

PCR_PARL_RX_RST_EN Configures whether or not to reset PARL RX module.

O: Not reset
1: Reset
(R/W)
```