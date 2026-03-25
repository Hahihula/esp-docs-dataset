

```markdown
Chapter 7 Reset and Clock

Register 7.19. PCR_TIMERGROUP1_TIMER_CLK_CONF_REG (0x0050)

PCR_TG1_TIMER_CLK_SEL Configures the clock source of general-purpose timers in Timer Group 1.
O (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F48M_CLK
3: No clock source
(R/W)

PCR_TG1_TIMER_CLK_EN Configures whether or not to enable the clock of general-purpose timers in Timer Group 1.
O: Not enable
1: Enable
(R/W)

Register 7.20. PCR_TIMERGROUP1_WDT_CLK_CONF_REG (0x0054)

PCR_TG1_WDT_CLK_SEL Configures the clock source of WDT in Timer Group 1.
O (default): XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
(R/W)

PCR_TG1_WDT_CLK_EN Configures whether or not to enable the clock for WDT in Timer Group 1.
O: Not enable
1: Enable
(R/W)
```