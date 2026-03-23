

```markdown
Chapter 8 Reset and Clock

Register 8.20. PCR_SYSTIMER_CONF_REG (0x0054)

PCR_SYSTIMER_CLK_EN Configures whether or not to enable SYSTIMER APB clock.
O: Not enable
1: Enable
(R/W)

PCR_SYSTIMER_RST_EN Configures whether or not to reset SYSTIMER module.
O: Not reset
1: Reset
(R/W)

Register 8.21. PCR_SYSTIMER_FUNC_CLK_CONF_REG (0x0058)

PCR_SYSTIMER_FUNC_CLK_SEL Configures to select clock source.
O (default): Select XTAL_CLK
1: Select RC_FAST_CLK
(R/W)

PCR_SYSTIMER_FUNC_CLK_EN Configures whether or not to enable SYSTIMER function clock.
O: Not enable
1: Enable
(R/W)
```