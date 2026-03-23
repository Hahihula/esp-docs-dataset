

```markdown
Register 12.67. RTC_TIMER_UPDATE_REG (0x0010)

| Bit | Description |
|-----|-------------|
| 31  | reserved    |
| 30  | O           |
| 29  | O           |
| 28  | O           |
| 27  | O           |
| ... | ...         |
| 0   | Reset       |

RTC_TIMER_MAIN_TIMER_SYS_RST Configures whether to trigger RTC timer upon system reset.
- 0: Do not trigger
- 1: Trigger (R/W)

RTC_TIMER_MAIN_TIMER_SYS_STALL Configures whether to trigger RTC timer when the CPU enters or exits stall state.
- 0: Do not trigger
- 1: Trigger (R/W)

RTC_TIMER_MAIN_TIMER_XTAL_OFF Configures whether to trigger RTC timer when PMU powers up or down the 40 MHz crystal.
- 0: Do not trigger
- 1: Trigger (R/W)

RTC_TIMER_UPDATE Configures whether to trigger RTC timer by software.
- 0: Do not trigger
- 1: Trigger (R/W)
```

Register 12.68. RTC_TIMER_MAIN_BUFO_LOW_REG (0x0014)

```markdown
| Bit | Description |
|-----|-------------|
| 31  | O           |
| ... | ...         |
| 0   | Reset       |

RTC_TIMER_MAIN_BUFO_LOW Register group 0 records the count value of the RTC timer, bit0 to bit31. (RO)
```