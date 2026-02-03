Title: Chapter 10 Low-power Management (RTC_CNTL)

Subtitle: GoBack

Section Title:
10.7 Register Summary

Body Text:

The addresses in this section are relative to low-power management base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

Table Headers: 
- Name
- Description
- Address
- Access

Table Content:

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| Control/Configuration Registers | Sets the power options of crystal and PLL clocks, and initiates reset by software | 0x0000 | varies |
| RTC_CNTL_RTC_OPTIONSO_REG |  |  | R/W |
| RTC_CNTL_RTC_SLT_TIMERO_REG | RTC timer threshold register 0 | 0x0004 | R/W |
| RTC_CNTL_RTC_SLP_TIMER1_REG | RTC timer threshold register 1 | 0x0008 | varies |
| RTC_CNTL_RTC_TIME_UPDATE_REG | RTC timer update control register | 0x000C | varies |
| RTC_CNTL_RTC_STATEO_REG | Configures the sleep/reject/wakeup state | 0x0018 | R/W |
| RTC_CNTL_RTC_TIMER1_REG | Configures CPU stall options | 0x001C | R/W |
| RTC_CNTL_RTC_TIMER2_REG | Configures RTC slow clock and touch controller | 0x0020 | R/W |
| RTC_CNTL_RTC_TIMERS5_REG | Configures the minimal sleep cycles | 0x002C | varies |
| RTC_CNTL_RTC_ANA_CONF_REG | Configures the power options for I2C and PLLA | 0x0034 | R/W |
| RTC_CNTL_RTC_WAKEUP_STAT_REG | Wakeup bitmap enabling register | 0x003C | R/W |
| RTC_CNTL_RTC_EXT_XTL_CONF_REG | 32 kHz crystal oscillator configuration register | 0x0060 | varies |
| RTC_CNTL_RTC_EXT_WAKEUP_CONF_REG | GPIO wakeup configuration register | 0x0064 | R/W |
| RTC_CNTL_RTC_SLP_REJECT_CONF_REG | Configures sleep/reject options | 0x0068 | R/W |
| RTC_CNTL_RTC_CLK_CONF_REG | RTC clock configuration register | 0x0074 | R/W |
| RTC_CNTL_RTC_SLOW_CLK_CONF_REG | RTC slow clock configuration register | 0x0078 | R/W |
| RTC_CNTL_RTC_SDIO_CONF_REG | configure flash power | 0x007C | varies |
| RTC_CNTL_RTC_REG | RTC/DIG regulator configuration register | 0x0084 | R/W |
| RTC_CNTL_RTC_PWC_REG | RTC power configuration register | 0x0088 | R/W |
| RTC_CNTL_DIG_PWC_REG | Digital system power configuration register | 0x0090 | varies |
| RTC_CNTL_DIG_ISO_REG | Digital system ISO configuration register | 0x0094 | varies |
| RTC_CNTL_RTC_WDTCONFIG0_REG | RTC watchdog configuration register | 0x0098 | R/W |
| RTC_CNTL_RTC_WDTCONFIG1_REG | Configures the hold time of RTC watchdog at level 1 | 0x009C | R/W |
| RTC_CNTL_RTC_WDTCONFIG2_REG | Configures the hold time of RTC watchdog at level 2 | 0x00A0 | varies |
| RTC_CNTL_RTC_WDTCONFIG3_REG | Configures the hold time of RTC watchdog at level 3 | 0x00A4 | R/W |
| RTC_CNTL_RTC_WDTCONFIG4_REG | Configures the hold time of RTC watchdog at level 4 | 0x00A8 | varies |
| RTC_CNTL_RTC_WDTFEED_REG | RTC watchdog SW feed configuration register | 0x00AC | WO |

Footer:
Espressif Systems
Submit Documentation Feedback

Page Number: ESP32-S3 TRM (Version 1.7)