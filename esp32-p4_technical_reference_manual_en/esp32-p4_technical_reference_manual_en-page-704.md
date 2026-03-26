

```markdown
Register 10.38. HP_SYS_CLKRST_PERI_CLK_CTRL20_REG (0x0094)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|---|---|
|     | HP_SYS_CLKRST_TIMERGRPO_TGRT_CLK_EN<br>HP_SYS_CLKRST_TIMERGRPO_WDT_CLK_EN<br>HP_SYS_CLKRST_TIMERGRPO_WDT_SRC_SEL<br>HP_SYS_CLKRST_TIMERGRPO_T1_CLK_EN<br>HP_SYS_CLKRST_TIMERGRPO_TO_CLK_EN<br>HP_SYS_CLKRST_MCPWM0_CLK_SRC_SEL<br>HP_SYS_CLKRST_MCPWM0_CLK_DIV_NUM<br>HP_SYS_CLKRST_MCPWM0_CLK_EN<br>HP_SYS_CLKRST_MCPWM1_CLK_SRC_SEL<br>HP_SYS_CLKRST_MCPWM1_CLK_DIV_NUM<br>HP_SYS_CLKRST_MCPWM1_CLK_EN |
| Value | 1 | 1 | 0 | 1 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

HP_SYS_CLKRST_MCPWM0_CLK_SRC_SEL Configures the clock source for MCPWM0_CLK.
0: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F160_CLK
3: Invalid
(R/W)

HP_SYS_CLKRST_MCPWM0_CLK_EN Configures whether to enable MCPWM0_CLK.
0: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_MCPWM0_CLK_DIV_NUM Configures the clock divisor of MCPWM0_CLK. (R/W)

HP_SYS_CLKRST_MCPWM1_CLK_SRC_SEL Configures the clock source for MCPWM1_CLK.
0: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F160_CLK
3: Invalid
(R/W)

HP_SYS_CLKRST_MCPWM1_CLK_EN Configures whether to enable MCPWM1_CLK.
0: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_MCPWM1_CLK_DIV_NUM Configures the clock divisor of MCPWM1_CLK. (R/W)

HP_SYS_CLKRST_TIMERGRPO_TO_SRC_SEL Configures the clock source for TIMER-GRPO_TO_CLK.
0: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
3: Invalid
(R/W)
```