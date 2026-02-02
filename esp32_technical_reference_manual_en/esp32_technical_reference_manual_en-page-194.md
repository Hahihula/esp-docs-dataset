**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Section Title:**
9.4 Register Summary

**Notes:**
- The registers listed below have been grouped according to their functionality. This particular grouping does not reflect the exact sequential order in which they are stored in memory.
- The base address for registers is 0x60008000 when accessed by AHB, and 0x3FF48000 when accessed by DPORT bus.

**Table:**
| Name | Description | Address | Access |
|------|-------------|---------|--------|
| RTC_CNTL_OPTIONSO_REG | Configure RTC options | 0x3FF48000 | R/W |
| **Control and configuration of RTC timer registers** | | | |
| RTC_CNTL_SLP_TIMERO_REG | RTC sleep timer | 0x3FF48004 | R/W |
| RTC_CNTL_SLP_TIMER1_REG | RTC sleep timer, alarm and control | 0x3FF48008 | R/W |
| RTC_CNTL_TIME_UPDATE_REG | Update control of RTC timer | 0x3FF4800C | RO |
| RTC_CNTL_TIMEO_REG | RTC timer low 32 bits | 0x3FF48010 | RO |
| RTC_CNTL_TIME1_REG | RTC timer high 16 bits | 0x3FF48014 | RO |
| RTC_CNTL_STATEO_REG | RTC sleep, SDIO and ULP control | 0x3FF48018 | R/W |
| RTC_CNTL_TIMER1_REG | CPU stall enable | 0x3FF4801C | R/W |
| RTC_CNTL_TIMER2_REG | Slow clock and touch controller configuration | 0x3FF48020 | R/W |
| RTC_CNTL_TIMER5_REG | Minimal sleep cycles in slow clock | 0x3FF4802C | R/W |
| **Reset state and wakeup control registers** | | | |
| RTC_CNTL_RESET_STATE_REG | Reset state control and cause of CPUs | 0x3FF48034 | RO |
| RTC_CNTL_WAKEUP_STATE_REG | Wake-up filter, enable and cause | 0x3FF48038 | RO |
| RTC_CNTL_EXT_WAKEUP_CONF_REG | Configuration of wake-up at low/high level | 0x3FF48060 | R/W |
| RTC_CNTL_EXT_WAKEUP1_REG | Selection of pads for external wake-up and wake-up clear bit | 0x3FF480CC | R/W |
| RTC_CNTL_EXT_WAKEUP1_STATUS_REG | External wake-up status | 0x3FF480D0 | RO |
| **RTC interrupt control and status registers** | | | |
| RTC_CNTL_INT_ENA_REG | Interrupt enable bits | 0x3FF4803C | R/W |
| RTC_CNTL_INT_RAW_REG | Raw interrupt status | 0x3FF48040 | RO |
| RTC_CNTL_INT_ST_REG | Masked interrupt status | 0x3FF48044 | RO |
| RTC_CNTL_INT_CLR_REG | Interrupt clear bits | 0x3FF48048 | WO |
| **RTC general purpose retention registers** | | | |
| RTC_CNTL_STOREO_REG | General purpose retention register 0 | 0x3FF4804C | R/W |
| RTC_CNTL STORE1_REG | General purpose retention register 1 | 0x3FF48050 | R/W |
| RTC_CNTL STORE2_REG | General purpose retention register 2 | 0x3FF48054 | R/W |
| RTC_CNTL STORE3_REG | General purpose retention register 3 | 0x3FF48058 | R/W |
| RTC_CNTL STORE4_REG | General purpose retention register 4 | 0x3FF480B0 | R/W |
| RTC_CNTL STORE5_REG | General purpose retention register 5 | 0x3FF480B4 | R/W |
| RTC_CNTL STORE6_REG | General purpose retention register 6 | 0x3FF480B8 | R/W |
| RTC_CNTL STORE7_REG | General purpose retention register 7 | 0x3FF480BC | R/W |

**Footer:**
Espressif Systems
194 ESP32 TRM (Version 5.6)
Submit Documentation Feedback