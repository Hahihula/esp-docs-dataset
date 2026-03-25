

```markdown
Register 9.43. PCR_PARL_CLK_RX_CONF_REG (0x00B0)

PCR_PARL_CLK_RX_DIV_NUM Configures the integral divisor for Parallel IO RX clock. (R/W)

PCR_PARL_CLK_RX_SEL Configures the clock source of Parallel IO RX.
O (default): XTAL
1: RC_FAST_CLK
2: PLL_F240M_CLK
3: Use the clock from chip pin
(R/W)

PCR_PARL_CLK_RX_EN Configures whether or not to enable Parallel IO RX clock.
O: Not enable
1: Enable
(R/W)

PCR_PARL_RX_RST_EN Configures whether or not to reset Parallel IO RX.
O: Not reset
1: Reset
(R/W)
```