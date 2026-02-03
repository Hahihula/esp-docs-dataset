**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Header:**
Register 10.14. RTC_CNTL_INT_ENA_RTC_REG (0x0040)

**Binary Register Diagram Description:**
The image shows a binary register with various fields labeled, each corresponding to different interrupt enable settings for the RTC_CNTL peripheral.

**Field Descriptions and Their Functions in Markdown Format:**

- **RTC_CNTL_TOUCH_APPROACH_LOOP_DONE_INT_ENA**: Enables interrupt when loop done. (R/W)
- **RTC_CNTL_TOUCH_DELTALINT_ENA**: Enables interrupt upon delta touch detection.
- **RTC_CNTL_TOUCHDeltaIntENa**: Enables interrupt for touch delta events.

**Interrupt Enable Fields:**
1. **RTC_CNTL_TOUCHDeltaIntENa**: Enables interrupt on touch delta event, with a binary representation of 0s and one set bit at position `3`.
2. **RTC_CNTL_TOUCHDeltaIntENa**: Enables interrupt upon the completion of an active touch.
3. **RTC_CNTL_TOUCHDeltaIntENa**: Enables interrupt when a single touch is detected.

**Interrupt Enable Fields (continued):**
1. **RTC_CNTL_SLP_WAKEUP_INT_ENA**: Enables interrupt on wake up from sleep, with binary representation showing multiple set bits at positions `2`, `4`, and others.
2. **RTC_CNTL_SLP_REJECT_INT_ENA**: Enables interrupt when the chip rejects to go into sleep.

**Other Interrupt Enable Fields:**
1. **RTC_CNTL_SDIO_IDLE_INT_ENA**: Enables interrupt upon SDIO idle state, with binary representation showing multiple set bits at positions `5`, `6`, and others.
2. **RTC_CNTL_RTC_WDT_INT_ENA**: Enables the RTC watchdog interrupt detection (R/W).
3. **RTC_CNTL_RTC_TOUCH_SCAN_DONE_INT_ENA**: Enables interrupt on touch scan completion.

**Additional Interrupt Enable Fields:**
1. **RTC_CNTL_RTC_ULP_CP_INT_ENA**: Enables ULP co-processor interrupt, with binary representation showing multiple set bits at positions `7`, `8`, and others.
2. **RTC_CNTL_RTC_TOUCH_DONE_INT_ENA**: Enables interrupt upon the single touch completion (R/W).
3. **RTC_CNTL_RTC TOUCH_ACTIVE_INT_ENA**: Enables interrupt when a touch is detected.

**Additional Interrupt Enable Fields:**
1. **RTC_CNTL_RTC_TOUCH_INACTIVE_INT_ENA**: Enables interrupt on release of active touch.
2. **RTC_CNTL_RTC_BROWN_OUT_INT_ENA**: Enables brown out interrupt detection (R/W).

**Footer Note:** Continued on the next page...

**Document Information at Bottom:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Link to Submit Documentation Feedback

This document provides detailed information about various interrupt enable settings for different events related to touch detection, sleep/wake states, watchdog interrupts, SDIO idle state, ULP co-processor operations in the RTC_CNTL peripheral of an ESP32-S3 chip by Espressif Systems.