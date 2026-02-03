**Chapter Title:**
Chapter 13 Watchdog Timers (WDT)

**Body Text:**

The write protection mechanism is implemented using a write-key field for each timer (TIMG_WDT_WKEY for MWDT, RTC_CNTL_WDT_WKEY or RWDT). The value 0x5D83AA1 must be written to the watchdog timer’s write-key field before any other register of the same watchdog timer can be changed. Any attempts to write to a watchdog timer's registers (other than the write-key field itself) whilst the write-key field’s value is not 0x5D83AA1 will be ignored. The recommended procedure for accessing a watchdog timer is as follows:

- Disable the write protection by writing the value 0x5D83AA1 to the timer's write-key field.
- Make the required modification of the watchdog such as feeding or changing its configuration.
- Re-enable write protection by writing any value other than 0x5D83AA1 to the timer’s write-key field.

**Subsection Title:**
13.2.2.4 Flash Boot Protection

**Body Text:**

During flash booting process, MWDT in timer group O (see Figure 12.1-1 Timer Units within Groups), as well as RWDT, are automatically enabled. Stage 0 for the enabled MWDT is automatically configured to reset the system upon expiry, known as core reset. Likewise, stage 0 for RWDT is configured to system reset, which resets the main system and RTC when it expires. After booting, TIMG_WDT_FLASHBOOT_MOD_EN and RTC_CNTL_WDT_FLASHBOOT_MOD_EN should be cleared to stop the flash boot protection procedure for both MWDT and RWDT respectively. After this, MWDT and RWDT can be configured by software.

**Subsection Title:**
13.3 Super Watchdog

**Body Text:**

Super watchdog (SWD) is an ultra-low-power circuit in analog domain that helps to prevent the system from operating in a sub-optimal state and resets the system if required. SWD contains a watchdog circuit that needs to be fed for at least once during its timeout period, which is slightly less than one second. About 100 ms before watchdog timeout, it will also send out a WD_INR signal as a request to remind the system to feed the watchdog.

If the system doesn’t respond to SWD feed request and watchdog finally times out, SWD will generate a system level signal SWD_RSTB to reset whole digital circuits on the chip.

**Subsection Title:**
13.3.1 Features

**List:**

- Ultra-low power
- Interrupt to indicate that the SWD timeout period is close to expiring
- Various dedicated methods for software to feed SWD, which enables SWD to monitor the working state of the whole operating system

**Subsection Title:**
13.3.2 Super Watchdog Controller

**Footer Text:**

Espressif Systems  
677  
ESP32-S3 TRM (Version 1.7)  

**Link Texts:**
- Submit Documentation Feedback
- GoBack