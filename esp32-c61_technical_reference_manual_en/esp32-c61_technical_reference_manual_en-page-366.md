

```markdown
Chapter 7 Reset and Clock

Register 7.41. PCR_IOMUX_CLK_CONF_REG (0x00C4)

PCR_IOMUX_FUNC_CLK_SEL Configures the clock source of IO MUX.
O (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
(R/W)

PCR_IOMUX_FUNC_CLK_EN Configures whether or not to enable IO MUX functional clock.
O: Not enable
1: Enable
(R/W)
```