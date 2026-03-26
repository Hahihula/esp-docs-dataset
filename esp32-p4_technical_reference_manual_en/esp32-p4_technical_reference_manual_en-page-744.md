

```markdown
Chapter 10 Reset and Clock

Register 10.60. LP_CLKRST_LP_CLK_EN_REG (0x0008)

LP_CLKRST_XTAL_CLK_FORCE_ON Configures whether to force on the XTAL_CLK control of LP CALI.
O: Controlled by hardware
1: Force on, bypassing hardware control
(R/W)

LP_CLKRST_CK_EN_LP_RAM Configurewhether to enable the clock of LP RAM.
O: Disable
1: Enable
(R/W)

LP_CLKRST_ETM_EVENT_TICK_EN Configures whether to enable the ETM event timer.
O: Disable
1: Enable
(R/W)

LP_CLKRST_PLL8M_CLK_FORCE_ON Configures whether to force on PLL_LP_CLK as LP_FAST_CLK source.
O: Controlled by hardware
1: Force on, bypassing hardware control
(R/W)

LP_CLKRST_XTAL_CLK_FORCE_ON Configures whether to force on XTAL_CLK as LP_FAST_CLK source.
O: Controlled by hardware
1: Force on, bypassing hardware control
(R/W)

LP_CLKRST_FOSC_CLK_FORCE_ON Configures whether to force on RC_FAST_CLK as LP_FAST_CLK source.
O: Controlled by hardware
1: Force on, bypassing hardware control
(R/W)
```