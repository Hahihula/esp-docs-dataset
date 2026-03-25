

```markdown
Chapter 7 Reset and Clock

Register 7.66. LP_CLKRST_LP_RST_EN_REG (0x0000C)

LP_CLKRST_ANA_PERI_RESET_EN
LP_CLKRST_WDT_RESET_EN
LP_CLKRST_LP_TIMER_RESET_EN
LP_CLKRST_AON_EFUSE_CORE_RESET_EN

(reserved)

| 31 | 30 | 29 | 28 | ... | 0 |
|-----|----:|----:|----:|-----|---|
|   0 |    0 |    0 |    0 | ... | Reset |

LP_CLKRST_AON_EFUSE_CORE_RESET_EN Configures whether to reset the always-on part of EFUSE_CTRL.
O: Invalid. No effect
1: Reset
(R/W)

LP_CLKRST_LP_TIMER_RESET_EN Configures whether to reset RTC timer.
O: Invalid. No effect
1: Reset
(R/W)

LP_CLKRST_WDT_RESET_EN Configures whether to reset RWDT and Super Watchdog Timer.
O: Invalid. No effect
1: Reset
(R/W)

LP_CLKRST_ANA_PERI_RESET_EN Configures whether to reset analog peripherals, including the Brownout Detector.
O: Invalid. No effect
1: Reset
(R/W)
```