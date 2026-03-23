

```markdown
PCR_PARL_CLK_TX_DIV_NUM Configures the integral part of the frequency divider factor for PARL TX clock.
(R/W)

PCR_PARL_CLK_TX_SEL Configures to select clock source.
0 (default): Select XTAL
1: Select PLL_F240M_CLK
2: Select RC_FAST_CLK
3: Use the clock from chip pin
(R/W)

PCR_PARL_CLK_TX_EN Configures whether or not to enable PARL TX clock.
0: Not enable
1: Enable
(R/W)

PCR_PARL_TX_RST_EN Configures whether or not to reset PARL TX module.
0: Not reset
1: Reset
(R/W)
```