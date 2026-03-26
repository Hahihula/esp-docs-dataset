

```markdown
Chapter 10 Reset and Clock

Register 10.38. HP_SYS_CLKRST_PERI_CLK_CTRL20_REG (0x0094)

Continued from the previous page...

HP_SYS_CLKRST_TIMERGRPO_TO_CLK_EN Configures whether to enable TIMERGRPO_TO_CLK.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_TIMERGRPO_T1_SRC_SEL Configures the clock source for TIMERGRPO_T1_CLK.
O: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
3: Invalid
(R/W)

HP_SYS_CLKRST_TIMERGRPO_T1_CLK_EN Configures whether to enable TIMERGRPO_T1_CLK.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_TIMERGRPO_WDT_SRC_SEL Configures the clock source for TIMER-
GRPO_WDT_CLK.
O: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
3: Invalid
(R/W)

HP_SYS_CLKRST_TIMERGRPO_WDT_CLK_EN Configures whether to enable TIMER-
GRPO_WDT_CLK.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_TIMERGRPO_TGRT_CLK_EN Configures whether to enable TIMER-
GRPO_TGRT_CLK.
O: Disable
1: Enable
(R/W)
```