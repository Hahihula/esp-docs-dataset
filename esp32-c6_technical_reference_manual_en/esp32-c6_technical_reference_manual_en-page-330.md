

```markdown
Register 8.16. PCR_TIMERGROUP0_WDT_CLK_CONF_REG (0x0044)

PCR_TGO_WDT_CLK_SEL   Configures to select clock source.
O (default): Select XTAL_CLK
1: Select PLL_F80M_CLK
2: Select RC_FAST_CLK
3: Reserved
(R/W)

PCR_TGO_WDT_CLK_EN    Configures whether or not to enable TIMER_GROUPO WDT clock.
O: Not enable
1: Enable
(R/W)
```

```markdown
Register 8.17. PCR_TIMERGROUP1_CONF_REG (0x0048)

PCR_TG1_CLK_EN        Configures whether or not to enable TIMER_GROUP1 APB clock.
O: Not enable
1: Enable
(R/W)

PCR_TG1_RST_EN        Configures whether or not to reset TIMER_GROUP1 module.
O: Not reset
1: Reset
(R/W)
```