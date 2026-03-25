

```markdown
Register 14.1. RTC_WDT_CONFIGO_REG (0x0000)

Continued from the previous page...

RTC_WDT_STG2 Configure the timeout action of stage2.
- 0: No action
- 1: Generate interrupt
- 2: Generate CPU reset
- 3: Generate core reset
- 4: Generate system reset
(R/W)

RTC_WDT_STG1 Configure the timeout action of stage1.
- 0: No action
- 1: Generate interrupt
- 2: Generate CPU reset
- 3: Generate core reset
- 4: Generate system reset
(R/W)

RTC_WDT_STGO Configure the timeout action of stage0.
- 0: No action
- 1: Generate interrupt
- 2: Generate CPU reset
- 3: Generate core reset
- 4: Generate system reset
(R/W)

RTC_WDT_EN Configure whether or not enable RWDT.
- 0: Disable RWDT
- 1: Enable RWDT
(R/W)
```

Register 14.2. RTC_WDT_CONFIG1_REG (0x0004)

```text
31                                                                                                 0
----------------------------------------------------------------------------------------------------
|                                                                                                 |
----------------------------------------------------------------------------------------------------
|                                                                                                 | Reset
----------------------------------------------------------------------------------------------------
200000

RTC_WDT_STGO_HOLD Configure the timeout time for stage0.
Measurement unit: RTC_DYN_SLOW_CLK
(R/W)
```

Espressif Systems

497

ESP32-H2 TRM (Version 1.1)

Submit Documentation Feedback