

```markdown
Register 15.24. TIMG_INT_CLR_TIMERS_REG (0x007C)

TIMG_TO_INT_CLR Write 1 to clear the TIMG_TO_INT interrupt. (WT)
TIMG_WDT_INT_CLR Write 1 to clear the TIMG_WDT_INT interrupt. (WT)

Register 15.25. TIMG_NTIMERS_DATE_REG (0x00F8)

TIMG_NTIMGS_DATE Version control register (R/W)

Register 15.26. TIMG_REGCLK_REG (0x00FC)

TIMG_ETM_EN Configures whether to enable timer's ETM task and event.
    0: Disable
    1: Enable
    (R/W)

TIMG_CLK_EN Configures whether to enable gate clock signal for registers.
    0: Force clock on for registers
    1: Support clock only when registers are read or written to by software.
    (R/W)
```