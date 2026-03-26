

```markdown
Register 10.39. HP_SYS_CLKRST_PERI_CLK_CTRL21_REG (0x0098)

| Bit | Field Name                                                                 | Description                                                                                                                                 |
|-----|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 31  | (reserved)                                                                  | -                                                                                                                                          |
| 30  | HP_SYS_CLKRST_SYSTIMER_CLK_EN                                               | -                                                                                                                                          |
| 29  | HP_SYS_CLKRST_SYSTIMER_CLK_SRC_SEL                                          | -                                                                                                                                          |
| 28  | HP_SYS_CLKRST_TIMERGRP1_WDT_CLK_EN                                         | -                                                                                                                                          |
| 27  | HP_SYS_CLKRST_TIMERGRP1_WDT_CLK_SRC_SEL                                    | -                                                                                                                                          |
| 26  | HP_SYS_CLKRST_TIMERGRP_T1_CLK_EN                                            | -                                                                                                                                          |
| 25  | HP_SYS_CLKRST_TIMERGRP_T1_CLK_SRC_SEL                                       | -                                                                                                                                          |
| 24  | HP_SYS_CLKRST_TIMERGRP_TO_CLK_EN                                             | -                                                                                                                                          |
| 23  | HP_SYS_CLKRST_TIMERGRP_TO_CLK_SRC_SEL                                       | -                                                                                                                                          |
| 22  | HP_SYS_CLKRST_TIMERGRP0_TGRT_CLK_DIV_NUM                                    | Configures the clock divisor of TIMERGRP0_TGRT_CLK. (R/W)                                                                                 |
| 21  |                                                                             | -                                                                                                                                          |
| 20  |                                                                             | -                                                                                                                                          |
| 19  |                                                                             | -                                                                                                                                          |
| 18  |                                                                             | -                                                                                                                                          |
| 17  |                                                                             | -                                                                                                                                          |
| 16  |                                                                             | -                                                                                                                                          |
| 15  |                                                                             | -                                                                                                                                          |
| 14  |                                                                             | -                                                                                                                                          |
| 13  |                                                                             | -                                                                                                                                          |
| 12-15| Clock tie 0 (R/W)                                                           | -                                                                                                                                          |

HP_SYS_CLKRST_TIMERGRP0_TGRT_CLK_SRC_SEL Configures the clock source for TIMERGRP0_TGRT_CLK.
0: MPLL_CLK (500 MHz)
1: SPLL_CLK (480 MHz)
2: CPLL_CLK (360 MHz)
3: APLL_CLK
4: SDIO_PLL0_CLK
5: SDIO_PLL1_CLK
6: SDIO_PLL2_CLK
7: RC_FAST_CLK
8: RC_SLOW_CLK
9: Invalid
10: XTAL32K_CLK
11: PLL_LP_CLK

HP_SYS_CLKRST_TIMERGRP0_TGRT_CLK_DIV_NUM Configures the clock divisor of TIMERGRP0_TGRT_CLK. (R/W)

HP_SYS_CLKRST_TIMERGRP1_TO_SRC_SEL Configures the clock source for TIMERGRP1_TO_CLK.
0: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F80M_CLK
3: Invalid
(R/W)

HP_SYS_CLKRST_TIMERGRP1_TO_CLK_EN Configures whether to enable TIMERGRP1_TO_CLK.
0: Disable
1: Enable
(R/W)
```