

```markdown
Register 9.21. PCR_TIMERGROUP0_TIMER_CLK_CONF_REG (0x0058)

PCR_TGO_TIMER_CLK_SEL   Configures the clock source of general-purpose timers in Timer Group O.
O (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F48M_CLK
3: No clock source
(R/W)

PCR_TGO_TIMER_CLK_EN    Configures whether or not to enable the clock of general-purpose timers in Timer Group O.
O: Not enable
1: Enable
(R/W)
```

```markdown
Register 9.22. PCR_TIMERGROUP0_WDT_CLK_CONF_REG (0x005C)

PCR_TGO_WDT_CLK_SEL     Configures the clock source of WDT in Timer Group O.
O (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
3: No clock source
(R/W)

PCR_TGO_WDT_CLK_EN      Configures whether or not to enable the clock of WDT in Timer Group O.
O: Not enable
1: Enable
(R/W)
```