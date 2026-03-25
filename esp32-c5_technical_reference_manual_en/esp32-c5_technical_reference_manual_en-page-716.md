

```markdown
Register 16.1. RTC_WDT_CONFIGO_REG (0x0000)

| Bit | 31 | 30 | 28 | 27 | 25 | 24 | 22 | 21 | 19 | 18 | 16 | 15 | 13 | 12 | 11 | 10 | 9 | 8 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|
|     | RTC_WDT_EN | RTC_WDT_STGO | RTC_WDT_STG1 | RTC_WDT_STG2 | RTC_WDT_STG3 | RTC_WDT_CPU_RESET_LENGTH | RTC_WDT_SYS_RESET_LENGTH | RTC_WDT_FLASHBOOT_MOD_EN | RTC_WDT_PROCPU_RESET_EN | RTC_WDT_PAUSE_IN_SLP | (reserved) |
| Value | 0x0 | 0x0 | 0x0 | 0x0 | 0x0 | 0x1 | 0x1 | 1 | 0 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

RTC_WDT_PAUSE_IN_SLP Configures whether or not to pause RWDT when chip is in Light-sleep or Deep-sleep mode.
O: Enable
1: Disable
(R/W)

RTC_WDT_PROCPU_RESET_EN Configures whether or not to enable RWDT to reset CPU.
O: Disable
1: Enable
(R/W)

RTC_WDT_FLASHBOOT_MOD_EN Configures whether or not to enable RWDT when chip is in SPI boot mode.
O: Disable
1: Enable
(R/W)

RTC_WDT_SYS_RESET_LENGTH Configures the core reset time.
Measurement unit: LP_DYN_FAST_CLK cycles
(R/W)

RTC_WDT_CPU_RESET_LENGTH Configures the CPU reset time.
Measurement unit: LP_DYN_FAST_CLK cycles
(R/W)

RTC_WDT_STG3 Configures the timeout action of stage3.
0: No operation
1: Generate interrupt
2: Generate CPU reset
3: Generate core reset
4: Generate system reset
(R/W)
```
Continued on the next page...
```