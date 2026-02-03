**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Subtitle:**
Register 10.17. RTC_CNTL_INT_CLR_RTC_REG (0x04C)

**Menu/Table Header:**
- RTC_CNTL
- RTC_TOUCH
- APPROACH_LOOP_DONE_INT_CLR
- RTC}_TOUCH
- DEL_INT_CLR
- RTC}_TOUCH
- TIME_OUT_INT_CLR
- RTC}_COGL
- CPU_TRAP_INT_CLR
- RTC}_COGL
- SWD_INT_CLR
- RTC}_COGL
- SARADC2K_INT_CLR
- RTC}_TSNS
- RTC}_BROWN_OUT_INACTIVE_INT_CLR
- RTC}_TOUCH
- ACTIVE_INT_CLR
- RTC}_TOUCH
- SCAN_DONE_INT_CLR
- RTC}_SDIO
- WDT_INT_CLR
- RTC}_IDLE
- RTC}_SLP_REJECT_INT_CLR
- RTC}_ULP
- SLEEP_INACTIVITY_INT_CLR
- RTC}_IDLE
- RTC}_SLP_WAKEUP_INT_CLR

**Body Text:**
1. **RTC_CNTL_WAKEUP_INT_CLR:** Clears the interrupt triggered when the chip wakes up from sleep.
2. **RTC_CNTL_SLP_REJECT_INT_CLR:** Clears the interrupt triggered when the chip rejects to go to sleep (WO).
3. **RTC_CNTL_SDIO_IDLE_INT_CLR:** Clears the interrupt triggered when the SDIO idles (WO).
4. **RTC_CNTL_RTC_WDT_INT_CLR:** Clears the RTC watchdog interrupt.
5. **RTC_CNTL_RTC TOUCH_SCAN_DONE_INT_CLR:** Clears the interrupt triggered upon completion of a touch scanning process.

6. **RTC_CNTL_RTC_ULP_CP_INT_CLR:** Clears the ULP co-processor interrupt
7. **RTC_CNTL_RTC_TOUCHDone_INT_CLR:** Clears the interrupt triggered when an active single touch is detected.
8. **RTC_CNTL_RTC TOUCH_ACTIVE_INT_CLR:** Clears the interrupt triggered upon a new touch detection.

9. **RTC_CNTL_RTC TOUCH_INACTIVE_INT_CLR:** Clears the interrupt triggered after release of all touches (WO).

10. **RTC_CNTL_RTC_BROWN_OUT_INT_CLR:** Clears brown out interrupts

**Footer:**
Continued on the next page...

**Document Information:**
- Page number: 601
- Document version: ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems
- Link text: Submit Documentation Feedback