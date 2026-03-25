

```markdown
Register 14.1. RTC_WDT_CONFIGO_REG (0x0000)

Continued from the previous page...

RTC_WDT_STG2 Configures the timeout action of stage2.
- 0: No operation
- 1: Generate interrupt
- 2: Generate CPU reset
- 3: Generate core reset
- 4: Generate system reset
(R/W)

RTC_WDT_STG1 Configures the timeout action of stage1.
- 0: No operation
- 1: Generate interrupt
- 2: Generate CPU reset
- 3: Generate core reset
- 4: Generate system reset
(R/W)

RTC_WDT_STGO Configures the timeout action of stage0.
- 0: No operation
- 1: Generate interrupt
- 2: Generate CPU reset
- 3: Generate core reset
- 4: Generate system reset
(R/W)

RTC_WDT_EN Configures whether or not enable RWDT.
- 0: Disable RWDT
- 1: Enable RWDT
(R/W)
```

```markdown
Register 14.2. RTC_WDT_CONFIG1_REG (0x0004)

RTC_WDT_STGO_HOLD Configures the timeout time for stage0.
Measurement unit: LP_DYN_SLOW_CLK cycles
(R/W)
```
```plaintext
31                                                                                                 0

┌───────────────────────────────────────────────────────────────────────────────────────────────┐
│200000                                                                                                                                              │Reset
└───────────────────────────────────────────────────────────────────────────────────────────────┘
```