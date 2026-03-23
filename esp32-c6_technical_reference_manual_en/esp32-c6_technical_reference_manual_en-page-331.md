

```markdown
Register 8.18. PCR_TIMERGROUP1_TIMER_CLK_CONF_REG (0x004C)

PCR_TG1_TIMER_CLK_SEL Configures to select clock source.
O (default): Select XTAL_CLK
1: Select PLL_F8OM_CLK
2: Select RC_FAST_CLK
3: Reserved
(R/W)

PCR_TG1_TIMER_CLK_EN Configures whether or not to enable TIMER_GROUP1 timer clock.
O: Not enable
1: Enable
(R/W)


Register 8.19. PCR_TIMERGROUP1_WDT_CLK_CONF_REG (0x0050)

PCR_TG1_WDT_CLK_SEL Configures to select clock source.
O (default): Select XTAL_CLK
1: Select PLL_F8OM_CLK
2: Select RC_FAST_CLK
3: Reserved
(R/W)

PCR_TG1_WDT_CLK_EN Configures whether or not to enable TIMER_GROUP1 WDT clock.
O: Not enable
1: Enable
(R/W)
```