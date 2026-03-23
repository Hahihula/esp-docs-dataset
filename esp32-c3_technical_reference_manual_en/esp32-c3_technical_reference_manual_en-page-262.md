

```markdown
Register 9.52. RTC_CNTL_XTAL32K_CONF_REG (0x00E8)

| Bit | Field Name                                 |
|-----|--------------------------------------------|
| 31  | OxO                                        |
| 30  | Oxff                                       |
| 27  | RTC_CNTL_XTAL32K_STABLE_THRES             |
| 26  |                                            |
| 25  |                                            |
| 24  |                                            |
| 23  |                                            |
| 22  |                                            |
| 21  |                                            |
| 20  | RTC_CNTL_XTAL32K_WDT_TIMEOUT              |
| 19  |                                            |
| 18  |                                            |
| 17  |                                            |
| 16  |                                            |
| 15  |                                            |
| 14  |                                            |
| 13  |                                            |
| 12  |                                            |
| 11  |                                            |
| 10  |                                            |
| 9   | RTC_CNTL_XTAL32K_RESTART_WAIT             |
| 8   |                                            |
| 7   |                                            |
| 6   |                                            |
| 5   |                                            |
| 4   | 0x00                                       |
| 3   | 0x0                                        |
| 2   | Reset                                      |
| 1   |                                            |
| 0   | RTC_CNTL_XTAL32K_RETURN_WAIT              |

RTC_CNTL_XTAL32K_RETURN_WAIT Defines the waiting cycles before returning to the normal XTAL32K oscillator. (R/W)

RTC_CNTL_XTAL32K_RESTART_WAIT Defines the waiting cycles before restarting the XTAL32K oscillator. (R/W)

RTC_CNTL_XTAL32K_WDT_TIMEOUT Defines the waiting period for clock detection. If no clock is detected after this period, the XTAL32K oscillator can be regarded as dead. (R/W)

RTC_CNTL_XTAL32K_STABLE_THRES Defines the allowed restarting period, within which the XTAL32K oscillator can be regarded as stable. (R/W)


Register 9.53. RTC_CNTL_USB_CONF_REG (0x00EC)

| Bit | Field Name                                 |
|-----|--------------------------------------------|
| 31  | (reserved)                                |
| 30  |                                            |
| 29  |                                            |
| 28  |                                            |
| 27  |                                            |
| 26  |                                            |
| 25  |                                            |
| 24  |                                            |
| 23  |                                            |
| 22  |                                            |
| 21  |                                            |
| 20  |                                            |
| 19  | (reserved)                                |
| 18  | RTC_CNTL_IO_MUX_RESET_DISABLE             |
| 17  |                                            |
| 16  |                                            |
| 15  |                                            |
| 14  |                                            |
| 13  |                                            |
| 12  |                                            |
| 11  |                                            |
| 10  |                                            |
| 9   |                                            |
| 8   |                                            |
| 7   |                                            |
| 6   |                                            |
| 5   |                                            |
| 4   |                                            |
| 3   |                                            |
| 2   |                                            |
| 1   |                                            |
| 0   | Reset                                      |

RTC_CNTL_IO_MUX_RESET_DISABLE Set this bit to disable io_mux reset. (R/W)
```