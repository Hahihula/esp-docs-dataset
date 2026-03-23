

```markdown
| Name                                       | Description                                                                                      | Address   | Access    |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|-----------|
| **TO control and configuration registers** |                                                                                                  |           |           |
| TIMG_TOCONFIG_REG                         | Timer 0 configuration register                                                                  | 0x0000    | varies    |
| TIMG_TOLO_REG                              | Timer 0 current value, low 32 bits                                                              | 0x0004    | RO        |
| TIMG_TOHI_REG                              | Timer 0 current value, high 22 bits                                                             | 0x0008    | RO        |
| TIMG_TOUPDATE_REG                          | Write to copy current timer value to TIMGn_TO_(LO/HI)_REG                                       | 0x000C    | R/W/SC    |
| TIMG_TOALARMLO_REG                         | Timer 0 alarm value, low 32 bits                                                                | 0x0010    | R/W       |
| TIMG_TOALARMIHI_REG                        | Timer 0 alarm value, high bits                                                                  | 0x0014    | R/W       |
| TIMG_TOLOADLO_REG                          | Timer 0 reload value, low 32 bits                                                               | 0x0018    | R/W       |
| TIMG_TOLOADHI_REG                          | Timer 0 reload value, high 22 bits                                                              | 0x001C    | R/W       |
| TIMG_TOLOAD_REG                            | Write to reload timer from TIMG_TO_(LOADLO/LOADHI)_REG                                         | 0x0020    | WT        |
| **WDT control and configuration registers**|                                                                                                  |           |           |
| TIMG_WDTCONFIG0_REG                        | Watchdog timer configuration register                                                          | 0x0048    | varies    |
| TIMG_WDTCONFIG1_REG                        | Watchdog timer prescaler register                                                               | 0x004C    | varies    |
| TIMG_WDTCONFIG2_REG                        | Watchdog timer stage 0 timeout value                                                           | 0x0050    | R/W       |
| TIMG_WDTCONFIG3_REG                        | Watchdog timer stage 1 timeout value                                                           | 0x0054    | R/W       |
| TIMG_WDTCONFIG4_REG                        | Watchdog timer stage 2 timeout value                                                           | 0x0058    | R/W       |
| TIMG_WDTCONFIG5_REG                        | Watchdog timer stage 3 timeout value                                                           | 0x005C    | R/W       |
| TIMG_WDTFEED_REG                            | Write to feed the watchdog timer                                                                | 0x0060    | WT        |
| TIMG_WDTWPROTECT_REG                        | Watchdog write protect register                                                                 | 0x0064    | R/W       |
| **RTC frequency calculation control and configuration registers** |                                                                                                  |           |           |
| TIMG_RTCCALICFG_REG                        | RTC frequency calculation configuration register 0                                             | 0x0068    | varies    |
| TIMG_RTCCALICFG1_REG                       | RTC frequency calculation configuration register 1                                             | 0x006C    | RO        |
| TIMG_RTCCALICFG2_REG                       | RTC frequency calculation configuration register 2                                             | 0x0080    | varies    |
| **Interrupt registers**                    |                                                                                                  |           |           |
| TIMG_INT_ENA_TIMERS_REG                    | Interrupt enable bits                                                                           | 0x0070    | R/W       |
| TIMG_INT_RAW_TIMERS_REG                    | Raw interrupt status                                                                            | 0x0074    | R/SS/WTC  |
| TIMG_INT_ST_TIMERS_REG                     | Masked interrupt status                                                                         | 0x0078    | RO        |
| TIMG_INT_CLR_TIMERS_REG                    | Interrupt clear bits                                                                            | 0x007C    | WT        |
| **Version register**                       |                                                                                                  |           |           |
| TIMG_NTIMERS_DATE_REG                      | Timer version control register                                                                  | 0x00F8    | R/W       |
| **Clock configuration registers**          |                                                                                                  |           |           |
| TIMG_REGCLKL_REG                            | Timer group clock gate register                                                                 | 0x00FC    | R/W       |
```