**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Header:**
Register 10.46. RTC_CNTL_RTC_LOW_POWER_ST_REG (0x00D0)

**Diagram Description and Labels:**
- The diagram shows a bit map with labels for different bits.
- Bits are labeled as follows:
  - RTC_CNTLMainStateInIdle
  - RTC_RdyForWakeup

**Bit Description Table:**
| Bit | Value |
|-----|-------|
| 31  | (reserved) |
| 26  | (reserved) |
| 27  | (reserved) |
| 26  | (reserved) |
| 20  | (reserved) |
| 19  | (reserved) |
| 18  | (reserved) |

**Text Descriptions:**
- **RTC_CNTL_RTC_RDY_FOR_WAKEUP**: Indicates the RTC is ready to be triggered by any wakeup source. (RO)
  
- **RTC_CNTL_MAIN_STATE_IN_IDLE**: Indicates the RTC state.
  - `0`: The chip can be either
    - in sleep modes.
    - entering sleep modes. In this case, wait until RTC_CNTL_RTC_RDY_FOR_WAKEUP bit is set, then you can wake up the chip.

  - `1`: Exiting sleep mode. In this case, RTC_CNTL_MAIN_STATE_IN_IDLE will eventually become 1.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback