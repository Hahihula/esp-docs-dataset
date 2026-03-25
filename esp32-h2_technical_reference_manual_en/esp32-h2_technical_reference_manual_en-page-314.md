

```markdown
Register 7.41. PCR_PARL_CLK_RX_CONF_REG (0x00A8)

PCR_PARL_CLK_RX_DIV_NUM Configures the integral divisor for Parallel IO RX clock. (R/W)

PCR_PARL_CLK_RX_SEL Configures the clock source of Parallel IO RX.
    0 (default): XTAL
    1: PLL_F96M_CLK
    2: RC_FAST_CLK
    3: Use the clock from chip pin
    (R/W)

PCR_PARL_CLK_RX_EN Configures whether or not to enable Parallel IO RX clock.
    0: Not enable
    1: Enable
    (R/W)

PCR_PARL_RX_RST_EN Configures whether or not to reset Parallel IO RX.
    0: Not reset
    1: Reset
    (R/W)
```