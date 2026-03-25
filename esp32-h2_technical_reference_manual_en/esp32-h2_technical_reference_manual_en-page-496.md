

```markdown
Register 14.1. RTC_WDT_CONFIGO_REG (0x0000)

| Bit | 31 | 30 | 28 | 27 | 25 | 24 | 22 | 21 | 19 | 18 | 16 | 15 | 13 | 12 | 11 | 10 | 9 | 8 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    | RTC_WDT_EN | RTC_WDT_STGO | RTC_WDT_STG1 | RTC_WDT_STG2 | RTC_WDT_STG3 | RTC_WDT_CPU_RESET_LENGTH | RTC_WDT_SYS_RESET_LENGTH | RTC_WDT_FLASHBOOT_MOD_EN | RTC_WDT_PROCPU_RESET_EN | (reserved) | RTC_WDT_PAUSE_IN_SLP | 0xO | 0xO | 0xO | 0xO | 0x1 | 0x1 |
|     |    |             |              |               |              |              |                           |                          |                         |                  |                 |        | Reset |

RTC_WDT_PAUSE_IN_SLP Configure whether or not to disable RWDT when chip is in sleep mode.
- O: Enable
- 1: Disable
(R/W)

RTC_WDT_PROCPU_RESET_EN Configure whether or not to enable RWDT to reset CPU.
- O: Disable
- 1: Enable
(R/W)

RTC_WDT_FLASHBOOT_MOD_EN Configure whether or not to enable RWDT when chip is in SPI boot mode.
- O: Disable
- 1: Enable
(R/W)

RTC_WDT_SYS_RESET_LENGTH Configure the core reset time.
Measurement unit: RTC_DYN_FAST_CLK
(R/W)

RTC_WDT_CPU_RESET_LENGTH Configure the CPU reset time.
Measurement unit: RTC_DYN_FAST_CLK
(R/W)

RTC_WDT_STG3 Configure the timeout action of stage3.
- 0: No action
- 1: Generate interrupt
- 2: Generate CPU reset
- 3: Generate core reset
- 4: Generate system reset
(R/W)
```