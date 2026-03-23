

```markdown
Register 14.26. TIMG_REGCLK_REG (0x00FC)
```

| Bit | 31 | 30 | 29 | 28 | ... | 0 |
|-----|----|----|----|----|-----|---|
|     | O  | 1  | 1  | 1  | 0   | Reset |

TIMG_ETM_EN Configures whether to enable timer's ETM task and event.
- 0: Disable
- 1: Enable (R/W)

TIMG_WDT_CLK_IS_ACTIVE Configures whether to enable WDT's clock.
- 0: Disable
- 1: Enable (R/W)

TIMG_TIMER_CLK_IS_ACTIVE Configures whether to enable Timer 0's clock.
- 0: Disable
- 1: Enable (R/W)

TIMG_CLK_EN Configures whether to enable gate clock signal for registers.
- 0: Force clock on for registers
- 1: Support clock only when registers are read or written to by software. (R/W)
```