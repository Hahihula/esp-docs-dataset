
```markdown
Register 9.7. RTC_CNTL_STATE0_REG (0x0018)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | RTC_CNTL_SLEEP_EN                                                           |
| 30  | RTC_CNTL_SLP_REJECT                                                       |
| 29  | RTC_CNTL_SLP_WAKEUP                                                      |
|     | (reserved)                                                                |
| 27  | RTC_CNTL_APB2RTC_BRIDGE_SEL                                              |
| 26  | (reserved)                                                                |
| 25  | RTC_CNTL_SLP_REJECT_CAUSE_CLR                                            |
| 24  | RTC_CNTL_SW_CPU_INT                                                       |
|     | Reset                                                                     |

RTC_CNTL_SW_CPU_INT Sends a SW RTC interrupt to CPU. (WO)
RTC_CNTL_SLP_REJECT_CAUSE_CLR Clears the RTC reject-to-sleep cause. (WO)
RTC_CNTL_APB2RTC_BRIDGE_SEL_1: APB to RTC using bridge (R/W)
RTC_CNTL_SLP_WAKEUP Sleep wakeup bit. (R/W)
RTC_CNTL_SLP_REJECT Sleep reject bit. (R/W)
RTC_CNTL_SLEEP_EN Sends the chip to sleep. (R/W)

Register 9.8. RTC_CNTL_TIMER1_REG (0x001C)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | RTC_CNTL_PLL_BUF_WAIT                                                      |
| 30  | RTC_CNTL_XTL_BUF_WAIT                                                     |
| 29  | RTC_CNTL_FOSC_WAIT                                                        |
|     | Reset                                                                     |

RTC_CNTL_CPU_STALL_EN Enables the CPU stalling. (R/W)
RTC_CNTL_CPU_STALL_WAIT Sets the CPU stall waiting cycles (using the RTC fast clock). (R/W)
RTC_CNTL_FOSC_WAIT Sets the FOSC clock waiting cycles (using the RTC slow clock). (R/W)
RTC_CNTL_XTL_BUF_WAIT Sets the XTAL waiting cycles (using the RTC slow clock). (R/W)
RTC_CNTL_PLL_BUF_WAIT Sets the PLL waiting cycles (using the RTC slow clock). (R/W)
```