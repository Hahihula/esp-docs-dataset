

```markdown
## Register 7.42. PCR_PARL_CLK_TX_CONF_REG (0x00AC)

PCR_PARL_CLK_TX_DIV_NUM Configures the integral divisor for Parallel IO TX clock. (R/W)

PCR_PARL_CLK_TX_SEL Configures the clock source of Parallel IO TX.
- O (default): XTAL
- 1: PLL_F96M_CLK
- 2: RC_FAST_CLK
- 3: Use the clock from chip pin
(R/W)

PCR_PARL_CLK_TX_EN Configures whether or not to enable Parallel IO TX clock.
- O: Not enable
- 1: Enable
(R/W)

PCR_PARL_TX_RST_EN Configures whether or not to reset Parallel IO TX.
- O: Not reset
- 1: Reset
(R/W)


## Register 7.43. PCR_GDMA_CONF_REG (0x00B8)

PCR_GDMA_CLK_EN Configures whether or not to enable GDMA clock.
- O: Not enable
- 1: Enable
(R/W)

PCR_GDMA_RST_EN Configures whether or not to reset GDMA.
- O: Not reset
- 1: Reset
(R/W)
```