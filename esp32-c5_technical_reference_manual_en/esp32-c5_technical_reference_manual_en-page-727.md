

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| **Configuration Registers**                |                                                                                                  |           |        |
| RTC_TIMER_TARO_LOW_REG                    | Configures the low 32 bits of the target time 0                                                 | 0x0000    | R/W    |
| RTC_TIMER_TARO_HIGH_REG                   | Configures the high 16 bits of the target time 0                                                | 0x0004    | varies |
| RTC_TIMER_TAR1_LOW_REG                    | Configures the low 32 bits of the target time 1                                                 | 0x0008    | R/W    |
| RTC_TIMER_TAR1_HIGH_REG                   | Configures the high 16 bits of the target time 1                                                | 0x000C    | varies |
| RTC_TIMER_UPDATE_REG                      | Configures to enable the RTC Timer to latch current value                                      | 0x0010    | varies |
| RTC_TIMER_MAIN_BUF0_LOW_REG               | The low 32 bits of the cached value 0 in RTC Timer                                              | 0x0014    | RO     |
| RTC_TIMER_MAIN_BUF0_HIGH_REG              | The high 16 bits of the cached value 0 in RTC Timer                                             | 0x0018    | RO     |
| RTC_TIMER_MAIN_BUF1_LOW_REG               | The low 32 bits of the cached value 1 in RTC Timer                                              | 0x001C    | RO     |
| RTC_TIMER_MAIN_BUF1_HIGH_REG              | The high 16 bits of the cached value 1 in RTC Timer                                             | 0x0020    | RO     |
| **Interrupt Registers**                    |                                                                                                  |           |        |
| RTC_TIMER_INT_RAW_REG                     | The interrupt raw status register for the RTC Timer reaching the target time 0                  | 0x0028    | R/WTC/SS|
| RTC_TIMER_INT_ST_REG                      | The interrupt status register for the RTC Timer reaching the target time 0                     | 0x002C    | RO     |
| RTC_TIMER_INT_ENA_REG                     | The interrupt enable register for the RTC Timer reaching the target time 0                     | 0x0030    | R/W    |
| RTC_TIMER_INT_CLR_REG                     | The interrupt clear register for the RTC Timer reaching the target time 0                      | 0x0034    | WT     |
| RTC_TIMER_LP_INT_RAW_REG                  | The interrupt raw status register for RTC Timer reaching the target time 1                     | 0x0038    | R/WTC/SS|
| RTC_TIMER_LP_INT_ST_REG                   | The interrupt status register for the RTC Timer reaching the target time 1                     | 0x003C    | RO     |
| RTC_TIMER_LP_INT_ENA_REG                  | The interrupt enable register for the RTC Timer reaching the target time 1                     | 0x0040    | R/W    |
| RTC_TIMER_LP_INT_CLR_REG                  | The interrupt clear register for the RTC Timer reaching the target time 1                      | 0x0044    | WT     |
| **Version Register**                       |                                                                                                  |           |        |
| RTC_TIMER_DATE_REG                        | Version control register                                                                        | 0x03FC    | R/W    |
```