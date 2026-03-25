

```markdown
Chapter 7 Reset and Clock

Register 7:16. PCR_TIMERGROUP0_TIMER_CLK_CONF_REG (0x0044)

PCR_TGO_TIMER_CLK_SEL   Configures the clock source of general-purpose timers in Timer Group O.
O (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
(R/W)

PCR_TGO_TIMER_CLK_EN    Configures whether or not to enable the clock of general-purpose timers in Timer Group O.
O: Not enable
1: Enable
(R/W)

Register 7:17. PCR_TIMERGROUP0_WDT_CLK_CONF_REG (0x0048)

PCR_TGO_WDT_CLK_SEL     Configures the clock source of WDT in Timer Group O.
O (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
(R/W)

PCR_TGO_WDT_CLK_EN      Configures whether or not to enable the clock of WDT in Timer Group O.
O: Not enable
1: Enable
(R/W)
```