

```markdown
Chapter 12 Low-Power Management

Register 12.78. RTC_TIMER_LP_INT_ENA_REG (0x0040)

RTC_TIMER_MAIN_TIMER_LP_INT_ENA
RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT_ENA

| 31 | 30 | 29 | reserved |
|-----:|----:|----:|----------|
| 0x0 | 0x0 |     |          |

RTC_TIMER_MAIN_TIMER_LP_INT_ENA Write 1 to enable RTC_TIMER_MAIN_TIMER_LP_INT. (RO)

RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT_ENA Write 1 to enable
RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT. (RO)

Register 12.79. RTC_TIMER_LP_INT_CLR_REG (0x0044)

RTC_TIMER_MAIN_TIMER_LP_INT_CLR
RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT_CLR

| 31 | 30 | 29 | reserved |
|-----:|----:|----:|----------|
| 0x0 | 0x0 |     |          |

RTC_TIMER_MAIN_TIMER_LP_INT_CLR Write 1 to clear RTC_TIMER_MAIN_TIMER_LP_INT. (RO)

RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT_CLR Write 1 to clear
RTC_TIMER_MAIN_TIMER_OVERFLOW_LP_INT. (RO)
```

## 12.10.4 Brownout Detector Registers

The addresses in this section are relative to the Low-power Analog Peripheral (LP_ANA_PERI) base address provided in Table 5.3-2 in Chapter 5 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.
```