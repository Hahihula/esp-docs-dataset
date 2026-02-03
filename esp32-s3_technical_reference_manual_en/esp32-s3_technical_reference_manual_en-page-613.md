**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Header:**
Register 10.32. RTC_CNTL_RTC_WDTCONFIGO_REG (0x0098)

**Table Description:**
- The table lists various registers related to the watchdog timer configuration in the RTC_CNTL register block.
- Columns include bit positions and names of each register.

**Text Content with Descriptions for Each Register:**

1. **RTC_CNTL_WDT_PAUSE_IN_SLP**: Set this bit to pause the watchdog in sleep mode (R/W).
2. **RTC_CNTL_WDT_APPCPU_RESET_EN**: Enable WDT reset APP CPU read/write.
3. **RTC_CNTL_WDT_PROCPUB_RESET_EN**: Set this bit to allow the watchdog to be able to reset CPU, R/W access is required for enabling or disabling it.

4. **RTC_CNTL_WDT_FLASHBOOT_MOD_EN**: Set this bit to enable watchdog when chip boots from flash (R/W).

5. **RTC_CNTL_WDT_SYS_RES_LENGTH**: Sets the length of the system reset counter.
6. **RTC_CNTL_WDT_CPU_RES_LENGTH**: Sets the length of the CPU reset counter.

7. **RTC_CNTL_WDT_STG3**: Enable at interrupt stage 2: enable at the CPU stage 3; enable at the system stage 4 (enable and read/write).

8. **RTC_CNTL_WDT_STG2**: Enable at interrupt stage 2, enable at the CPU stage 3.
9. **RTC_CNTL_WDT_STG1**: Enable at interrupt stage 2.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Version Information:**
ESP32-S3 TRM (Version 1.7)