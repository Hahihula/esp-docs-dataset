

```markdown
Register 8.14. PCR_TIMERGROUP0_CONF_REG (0x003C)

PCR_TGO_CLK_EN Configures whether or not to enable TIMER_GROUP0 APB clock.
O: Not enable
1: Enable
(R/W)

PCR_TGO_RST_EN Configures whether or not to reset TIMER_GROUP0 module.
O: Not reset
1: Reset
(R/W)
```

```markdown
Register 8.15. PCR_TIMERGROUP0_TIMER_CLK_CONF_REG (0x0040)

PCR_TGO_TIMER_CLK_SEL Configures to select clock source.
O (default): Select XTAL_CLK
1: Select PLL_F80M_CLK
2: Select RC_FAST_CLK
3: Reserved
(R/W)

PCR_TGO_TIMER_CLK_EN Configures whether or not to enable TIMER_GROUP0 timer clock.
O: Not enable
1: Enable
(R/W)
```