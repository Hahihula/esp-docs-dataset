
```markdown
| Name                                       | Description                                                                                      | Address   | Access    |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|-----------|
| RTC_CNTL_OPTIONSO_REG                     | Sets the power options of crystal and PLL clocks, and initiates reset by software                | 0x0000    | Varies    |
| RTC_CNTL_SLP_TIMERO_REG                   | RTC timer threshold register 0                                                                  | 0x0004    | R/W       |
| RTC_CNTL_SLP_TIMER1_REG                   | RTC timer threshold register 1                                                                  | 0x0008    | varies    |
| RTC_CNTL_TIME_UPDATE_REG                  | RTC timer update control register                                                               | 0x000C    | varies    |
| RTC_CNTL_TIME_LOWRO_REG                   | Stores the lower 32 bits of RTC timer 0                                                         | 0x0010    | RO        |
| RTC_CNTL_TIME_HIGHRO_REG                  | Stores the higher 16 bits of RTC timer 0                                                       | 0x0014    | RO        |
| RTC_CNTL_STATEO_REG                       | Configures the sleep / reject / wakeup state                                                   | 0x0018    | varies    |
| RTC_CNTL_TIMER1_REG                       | Configures CPU stall options                                                                    | 0x001C    | R/W       |
| RTC_CNTL_TIMER2_REG                       | Configures RTC slow clock and touch controller                                                | 0x0020    | R/W       |
| RTC_CNTL_TIMER5_REG                       | Configures the minimal sleep cycles                                                             | 0x002C    | R/W       |
| RTC_CNTL_ANA_CONF_REG                     | Configures the power options for I2C and PLLLA                                                | 0x0034    | R/W       |
| RTC_CNTL_RESET_STATE_REG                  | Indicates the CPU reset source                                                                  | 0x0038    | varies    |
| RTC_CNTL_WAKEUP_STATE_REG                 | Wakeup bitmap enabling register                                                                 | 0x003C    | R/W       |
| RTC_CNTL_INT_ENA_RTC_REG                  | RTC interrupt enabling register                                                                 | 0x0040    | R/W       |
| RTC_CNTL_INT_RAW_RTC_REG                  | RTC interrupt raw register                                                                      | 0x0044    | RO        |
| RTC_CNTL_INT_ST_RTC_REG                   | RTC interrupt state register                                                                    | 0x0048    | RO        |
| RTC_CNTL_INT_CLR_RTC_REG                  | RTC interrupt clear register                                                                    | 0x004C    | WO        |
| RTC_CNTL_STOREO_REG                       | Reservation register 0                                                                          | 0x0050    | R/W       |
| RTC_CNTL_STORE1_REG                       | Reservation register 1                                                                          | 0x0054    | R/W       |
| RTC_CNTL_STORE2_REG                       | Reservation register 2                                                                          | 0x0058    | R/W       |
| RTC_CNTL_STORE3_REG                       | Reservation register 3                                                                          | 0x005C    | R/W       |
| RTC_CNTL_EXT_XTL_CONF_REG                 | 32 kHz crystal oscillator configuration register                                               | 0x0060    | varies    |
| RTC_CNTL_EXT_WAKEUP_CONF_REG              | GPIO wakeup configuration register                                                              | 0x0064    | R/W       |
| RTC_CNTL_SLP_REJECT_CONF_REG              | Configures sleep / reject options                                                               | 0x0068    | R/W       |
| RTC_CNTL_CLK_CONF_REG                     | RTC timer configuration register                                                               | 0x0070    | R/W       |
| RTC_CNTL_SLOW_CLK_CONF_REG                | RTC slow clock configuration register                                                          | 0x0074    | R/W       |
| RTC_CNTL_REG                              | RTC configuration register                                                                      | 0x0080    | R/W       |
| RTC_CNTL_PWC_REG                          | RTC power configuration register                                                               | 0x0084    | R/W       |
| RTC_CNTL_DIG_PWC_REG                      | Digital system power configuration register                                                    | 0x0088    | R/W       |
| RTC_CNTL_DIG_ISO_REG                      | Digital system isolation configuration register                                                | 0x008C    | varies    |
| RTC_CNTL_WDTCONFIGO_REG                   | RTC watchdog configuration register                                                            | 0x0090    | R/W       |
| RTC_CNTL_WDTCONFIG1_REG                   | Configures the hold time of RTC watchdog at level 1                                            | 0x0094    | R/W       |
```