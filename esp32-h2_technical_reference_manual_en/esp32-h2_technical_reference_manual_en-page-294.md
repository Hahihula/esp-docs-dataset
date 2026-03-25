

```markdown
Register 7.13. PCR_RMT_SCLK_CONF_REG (0x0038)

PCR_RMT_SCLK_DIV_A Configures the denominator of the divisor's fractional part for RMT functional clock. (R/W)

PCR_RMT_SCLK_DIV_B Configures the numerator of the divisor's fractional part for RMT functional clock. (R/W)

PCR_RMT_SCLK_DIV_NUM Configures the integral part of the divisor for RMT functional clock. (R/W)

PCR_RMT_SCLK_SEL Configures the clock source of RMT.
O: XTAL_CLK
1 (default): RC_FAST_CLK
(R/W)

PCR_RMT_SCLK_EN Configures whether or not to enable RMT functional clock.
O: Not enable
1: Enable
(R/W)
```