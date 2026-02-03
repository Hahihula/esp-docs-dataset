**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Header:**
GoBack

**Subheader:**
Register 10.12. RTC_CNTL_RTC_RESET_STATE_REG (0x0038)

**Diagram Description:**
A bit map diagram showing the layout of register bits from 31 to 0, with labels for each bit and its corresponding function.

**Bit Labels and Functions:**

- **RTC_CNTL_RESET_CAUSE_PROCPUB**: Stores CPU0's reset cause. (RO)
- **RTC_CNTL_RESET_CAUSE_APPCPU**: Stores CPU1’s reset cause. (RO)
- **RTC_CNTL_APPCPU_STATE_VECTOR_SEL**: Selects CPU1 state vector. (R/W)
- **RTC_CNTL_PROCPU_STATE_VECTOR_SEL**: Selects CPU0 state vector. (R/W)
- **RTC_CNTL_RESET_FLAG_PROCPUB**: Sets CPU0 reset flag. (RO)
- **RTC_CNTL_RESET_FLAG_APPCPU**: Sets CPU1 reset flag. (RO)
- **RTC_CNTL_RESET_FLAG_PROCPUB_CLR**: Set this bit to clear CPU0 reset flag. (WO)
- **RTC_CNTL_RESET_FLAG_APPCPU_CLR**: Set this bit to clear CPU1 reset flag. (WO)
- **RTC_CNTL_APPCPU_OCD_HALT_ON_RESET**: Enables CPU1 to enter halt state after reset. (R/W)
- **RTC_CNTL_PROCPU_OCD_HALT_ON_RESET**: Enables CPU0 to enter halt state after reset. (R/W)
- **RTC_CNTL_RESET_FLAG_UTAG_PROCPUB**: CPU's JTAG reset flag. (RO)
- **RTC_CNTL_RESET_FLAG_UTAG_APPCPU**: CPU1’s JTAG reset flag. (RO)
- **RTC_CNTL_RESET_FLAGUTAG_PROCPUB_CLR**: Set this bit to clear CPU0 JTAG reset flag. (WO)
- **RTC_CNTL_RESET_FLAGUTAG_APPCPU_CLR**: Set this bit to clear CPU1 JTAG reset flag. (WO)
- **RTC_CNTL_RTC_APP_DRESET_MASK**: Set this bit to bypass CPU1 dreset. (R/W)
- **RTC_CNTL_RTC_PRO_DRESET_MASK**: Set this bit to bypass CPU0 dreset. (R/W)

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)