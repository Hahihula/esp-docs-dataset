

```markdown
Chapter 9 Low-power Management

Register 9.48. RTC_CNTL_BROWN_OUT_REG (0x00D8)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 |                                                                             |
| 30  |                                 |                                                                             |
| 29  |                                 |                                                                             |
| 28  |                                 |                                                                             |
| 27  |                                 |                                                                             |
| 26  |                                 |                                                                             |
| 25  |                                 |                                                                             |
|     |                                 |                         (reserved)                                          |
| 16  |                                 |                                                                             |
| 15  |                                 |                                                                             |
| 14  |                                 |                                                                             |
| 13  |                                 |                                                                             |
| 4   |                                 |                                                                             |
| 3   |                                 |                                                                             |
| 0   |                                 |                                                                             |

RTC_CNTL_BROWN_OUT_INT_WAIT Configures the waiting cycles before sending an interrupt. (R/W)

RTC_CNTL_BROWN_OUT_CLOSE_FLASH_ENA Set this bit to enable PD the flash when a brown-out happens. (R/W)

RTC_CNTL_BROWN_OUT_PD_RF_ENA Set this bit to enable PD the RF circuits when a brown-out happens. (R/W)

RTC_CNTL_BROWN_OUT_RST_WAIT Configures the waiting cycles before the reset after a brown-out. (R/W)

RTC_CNTL_BROWN_OUT_RST_ENA Enables to reset brown-out. (R/W)

RTC_CNTL_BROWN_OUT_RST_SEL Selects the reset type when a brown-out happens. 1: chip reset, 0: system reset. (R/W)

RTC_CNTL_BROWN_OUT_ANA_RST_EN Enables to reset brown-out. (R/W)

RTC_CNTL_BROWN_OUT_CNT_CLR Clears the brown-out counter. (WO)

RTC_CNTL_BROWN_OUT_ENA Set this bit to enable brown-out detection. (R/W)

RTC_CNTL_BROWN_OUT_DET Indicates the status of the brown-out signal. (RO)


Register 9.49. RTC_CNTL_TIME_LOW1_REG (0x0DDC)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 |                                                                             |
|     |                                 |                         0                                                     |
|     |                                 |                         Reset                                                |

RTC_CNTL_TIMER_VALUE1_LOW Stores the lower 32 bits of RTC timer 1. (RO)
```