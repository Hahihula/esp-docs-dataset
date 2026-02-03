**Title: Chapter 10 Low-power Management (RTC_CNTL)**

**Header: Register 10.51. RTC_CNTL_RTC_BROWN_OUT_REG (0x00E8)**

| Bit Field | Name | Description |
|-----------|------|-------------|
| 31-29     | RTC_CNTL_RTC_BROWN_OUT_DET | Brown-out detected interrupt flag |
| 28        | RTC_CNTL_RTC_BROWN_OUT_CLR | Clear brown-out interrupt flag |
| 27        | RTC_CNTL_RTC_BROWN_OUT_ANA_RST_SEL | Analog reset selection for brown-out |
| 26-15     | RTC_CNTL_RTC_BROWN_OUT_PD_RF_ENA | Power down RF circuits during brown-out |
| 14-8      | RTC_CNTL_RTC_BROWN_OUT_RST_WAIT | Enable waiting cycle before the reset after a brown-out happens |
| 7         | RTC_CNTL_RTC_BROWN_OUT_CLOSE_FLASH_ENA | Enable PD flash when a brown-out happens |
| 6         | RTC_CNTL_RTC_BROWN_OUT_PD_RF_ENA | Power down RF circuits during brown-out |
| 5-0       | RTC_CNTL_RTC_BROWN_OUT_RST_WAIT | Configure the waiting cycle before reset after a brown-out. |

**Body Text:**

- **RTC_CNTL_BROWN_OUT_INT_WAIT**: Configures the waiting cycle before sending an interrupt.
- **RTC_CNTL_BROWN_OUT_CLOSE_FLASH_ENA**: Set this bit to enable PD flash when a brown-out happens (R/W).
- **RTC_CNTL_BROWN_OUT_PD_RF_ENA**: Set this bit to enable power down RF circuits during a brown-out. 
- **RTC_CNTL_BROWN_OUT_RST_WAIT**: Configures the waiting cycle before reset after a brown-out.
- **RTC_CNTL_BROWN_OUT_RST_ENA**: Enables to reset out (R/W).
- **RTC_CNTL_BROWN_OUT_RST_SEL**: Selects chip type when happens: 1: Chip reset; System reset. 
- **RTC_CNTL_BROWN_OUT_ANA_RST_EN**: Enables power down RF circuits during a brown-out.
- **RTC_CNTL_BROWN_OUT_CNT_CLR**: Clears the counter (W).
- **RTC_CNTL_BROWN_OUT_ENA**: Set this bit to enable out detection.

**Footer:**

Espressif Systems  
623 ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)