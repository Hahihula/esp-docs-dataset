**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Header:**
Register 10.16. RTC_CNTL_INT_ST_RTC_REG (0x048)

**Menu/Navigation Link:**
GoBack

**Diagram/Table Description:**
A table with a list of interrupt status registers for the RTC_CNTL module, each labeled as "RTC_CNTL_XXX_INT_ST" where XXX represents different types such as TOUCH, APPROACH, LOOPDONE, etc. Each entry in this column is followed by its corresponding bit positions from 31 to 0.

**List of Interrupt Status Registers:**
- **RTC_CNTL_SLP_WAKEUP_INT_ST**: Stores the status of the interrupt triggered when the chip wakes up from sleep.
- **RTC_CNTL_SLP_REJECT_INT_ST**: Stores the status of the interrupt triggered when the chip rejects to go to sleep.
- **RTC_CNTL_SDIO_IDLE_INT_ST**: Stores the status of the interrupt triggered when the SDIO idles (RO).
- **RTC_CNTL_RTC_WDT_INT_ST**: Stores the status of the RTC watchdog interrupt. (RO)
- **RTC_CNTL_RTC TOUCH_SCAN_DONE_INT_ST**: Stores the status of the interrupt triggered upon completion of a touch scanning.
- **RTC_CNTL_RTC_ULP_CP_INT_ST**: Stores the status of the ULP co-processor interrupt. (RO)
- **RTC_CNTL_RTC_TOUCHDONE_INT_ST**: Stores the status of the interrupt triggered upon the completion of a single touch. (RO)
- **RTC_CNTL_RTC TOUCH_ACTIVE_INT_ST**: Stores the status of the interrupt triggered when a touch is detected.
- **RTC_CNTL_RTC TOUCH_INACTIVE_INT_ST**: Stores the status of the interrupt triggered when a touch is released.

**Footer:**
Continued on the next page...

**Document Information:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version:**
599 ESP32-S3 TRM (Version 1.7)