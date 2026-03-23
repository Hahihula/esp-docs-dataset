

```markdown
| Name                        | Description                                                                 | Address | Access |
|-----------------------------|-----------------------------------------------------------------------------|---------|--------|
| LP_AON_LPBUS_REG            | LP SRAM access mode configuration register                                  | 0x0048  | varies |
```

## 12.9.3 RTC Timer Register Summary

The addresses in this section are relative to the RTC Timer base address provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| **Configuration Registers**                |                                                                             |         |        |
| RTC_TIMER_TARO_LOW_REG                    | Configures the low 32 bits of the target count value 0 of the RTC timer.    | 0x0000  | R/W    |
| RTC_TIMER_TARO_HIGH_REG                   | Configures the high 16 bits of the target count value 0 of the RTC timer.   | 0x0004  | R/W    |
| RTC_TIMER_TAR1_LOW_REG                    | Configures the low 32 bits of the target count value 1 of the RTC timer.    | 0x0008  | R/W    |
| RTC_TIMER_TAR1_HIGH_REG                   | Configures the high 16 bits of the target count value 1 of the RTC timer.   | 0x000C  | R/W    |
| RTC_TIMER_UPDATE_REG                      | RTC timer value record register                                            | 0x0010  | R/W    |
| RTC_TIMER_MAIN_BUF0_LOW_REG               | RTC timer register group0, bit0 - bit31                                    | 0x0014  | RO     |
| RTC_TIMER_MAIN_BUF0_HIGH_REG              | RTC timer register group0, bit32 - bit47                                   | 0x0018  | RO     |
| RTC_TIMER_MAIN_BUF1_LOW_REG               | RTC timer register group1, bit0 - bit31                                    | 0x001C  | RO     |
| RTC_TIMER_MAIN_BUF1_HIGH_REG              | RTC timer register group1, bit32 - bit47                                   | 0x0020  | RO     |
| RTC_TIMER_INT_RAW_REG                     | LP_RTC_TIMER_INT raw interrupt                                            | 0x0028  | RO     |
| RTC_TIMER_INT_ST_REG                      | LP_RTC_TIMER_INT state interrupt                                          | 0x002C  | RO     |
| RTC_TIMER_INT_ENA_REG                     | LP_RTC_TIMER_INT interrupt enable register                                | 0x0030  | R/W    |
| RTC_TIMER_INT_CLR_REG                     | LP_RTC_TIMER_INT interrupt clear register                                 | 0x0034  | WT     |
| RTC_TIMER_LP_INT_RAW_REG                  | LP_RTC_TIMER_LP_INT raw interrupt                                         | 0x0038  | RO     |
| RTC_TIMER_LP_INT_ST_REG                   | LP_RTC_TIMER_LP_INT state interrupt                                      | 0x003C  | RO     |
| RTC_TIMER_LP_INT_ENA_REG                  | LP_RTC_TIMER_LP_INT interrupt enable register                            | 0x0040  | R/W    |
| RTC_TIMER_LP_INT_CLR_REG                  | LP_RTC_TIMER_LP_INT interrupt clear register                              | 0x0044  | WT     |

## 12.9.4 Brownout Detector Register Summary

The addresses in this section are relative to the Low-power Analog Peripheral (LP_ANA_PERI) base address provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.
```