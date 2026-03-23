

```markdown
## Register 9.38. RTC_CNTL_SWD_CONF_REG (0x0DAC)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | Reserved                                   |                                                                             |
| 30  | RTC_CNTL_SWD_AUTO_FEED_EN                  | Set this bit to enable automatic watchdog feeding upon interrupts. (R/W)      |
| 29  | RTC_CNTL_SWD_DISABLE                       | Set this bit to disable super watchdog. (R/W)                                |
| 28  | RTC_CNTL_SWD_FEED                          | Set to feed the super watchdog via SW. (WO)                                  |
| 27  | RTC_CNTL_SWD_RST_FLAG_CLR                  | Set to reset the super watchdog reset flag. (WO)                             |
| 26  | RTC_CNTL_SWD_SIGNAL_WIDTH                  | Adjusts the signal width sent to the super watchdog. (R/W)                   |
| 25  | RTC_CNTL_SWD_BYPASS_RST                    | Set this bit to bypass super watchdog reset. (R/W)                           |
| 24  | RTC_CNTL_SWD_FEED_INT                      | Receiving this interrupt leads to feeding the super watchdog via SW. (RO)    |
| 23  | RTC_CNTL_SWD_RESET_FLAG                    | Indicates the super watchdog reset flag. (RO)                                |
| 15-0| Reserved                                   |                                                                             |

RTC_CNTL_SWD_RESET_FLAG Indicates the super watchdog reset flag. (RO)
RTC_CNTL_SWD_FEED_INT Receiving this interrupt leads to feeding the super watchdog via SW.
(RO)
RTC_CNTL_SWD_BYPASS_RST Set this bit to bypass super watchdog reset. (R/W)
RTC_CNTL_SWD_SIGNAL_WIDTH Adjusts the signal width sent to the super watchdog. (R/W)
RTC_CNTL_SWD_RST_FLAG_CLR Set to reset the super watchdog reset flag. (WO)
RTC_CNTL_SWD_FEED Set to feed the super watchdog via SW. (WO)
RTC_CNTL_SWD_DISABLE Set this bit to disable super watchdog. (R/W)
RTC_CNTL_SWD_AUTO_FEED_EN Set this bit to enable automatic watchdog feeding upon interrupts. (R/W)

## Register 9.39. RTC_CNTL_SWD_WPROTECT_REG (0x00B0)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | Reserved                                   |                                                                             |
| 30-0| RTC_CNTL_SWD_WKEY                         | Sets the write protection key of the super watchdog. (R/W)                   |

RTC_CNTL_SWD_WKEY Sets the write protection key of the super watchdog. (R/W)
```