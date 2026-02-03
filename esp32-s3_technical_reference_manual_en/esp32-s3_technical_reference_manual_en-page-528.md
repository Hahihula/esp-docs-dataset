**Chapter Title:**
Chapter 7 Reset and Clock

**Table Header:**
- Code
- Source
- Reset Type
- Comments

**Table Content (structured as rows):**

1. **Code:** 0x01  
   **Source:** Chip reset  
   **Reset Type:** Chip Reset  
   **Comments:** -

2. **Code:** 0x0F  
   **Source:** Brown-out system reset  
   **Reset Type:** Chip Reset or System Reset  
   **Comments:** Triggered by brown-out detector²

3. **Code:** 0x10  
   **Source:** RWDT system reset  
   **Reset Type:** System Reset  
   **Comments:** See Chapter 13 Watchdog Timers (WDT)

4. **Code:** 0x12  
   **Source:** Super Watchdog reset  
   **Reset Type:** System Reset  
   **Comments:** See Chapter 13 Watchdog Timers (WDT)

5. **Code:** 0x13  
   **Source:** GLITCH reset  
   **Reset Type:** System Reset  
   **Comments:** See Chapter 24 Clock Glitch Detection

6. **Code:** 0x03  
   **Source:** Software system reset  
   **Reset Type:** Core Reset  
   **Comments:** Triggered by configuring RTC_CNTL_SW_SYS_RST

7. **Code:** 0x05  
   **Source:** Deep-sleep reset  
   **Reset Type:** Core Reset  
   **Comments:** See Chapter 10 Low-power Management (RTC_CNTL)

8. **Code:** 0x07  
   **Source:** MWDTO core reset  
   **Reset Type:** Core Reset  
   **Comments:** See Chapter 13 Watchdog Timers (WDT)

9. **Code:** 0x08  
   **Source:** MWDT1 core reset  
   **Reset Type:** Core Reset  
   **Comments:** See Chapter 13 Watchdog Timers (WDT)

10. **Code:** 0x09  
    **Source:** RWDT core reset  
    **Reset Type:** Core Reset  
    **Comments:** See Chapter 13 Watchdog Timers (WDT)

11. **Code:** 0x14  
    **Source:** eFuse reset  
    **Reset Type:** Core Reset  
    **Comments:** Triggered by eFuse CRC error

12. **Code:** 0x15  
    **Source:** USB (UART) reset  
    **Reset Type:** Core Reset  
    **Comments:** Triggered when external USB host sends a specific command to the Serial interface of USB-Serial-JTAG. See [33 USB Serial/JTAG Controller](#USB_SERIAL_JTAG)

13. **Code:** 0x16  
    **Source:** USB (JTAG) reset  
    **Reset Type:** Core Reset  
    **Comments:** Triggered when external USB host sends a specific command to the JTAG interface of USB-Serial-JTAG. See [33 USB Serial/JTAG Controller](#USB_SERIAL_JTAG)

14. **Code:** 0x0B  
    **Source:** MWDTO CPU reset  
    **Reset Type:** CPU Reset  
    **Comments:** See Chapter 13 Watchdog Timers (WDT)

15. **Code:** 0x0C  
    **Source:** Software CPU reset  
    **Reset Type:** CPU Reset  
    **Comments:** Triggered by configuring RTC_CNTL_SW_PROCPU/APPCPU_RST

16. **Code:** 0x0D  
    **Source:** RWDT CPU reset  
    **Reset Type:** CPU Reset  
    **Comments:** See Chapter 13 Watchdog Timers (WDT)

17. **Code:** 0x11  
    **Source:** MWDT1 CPU reset  
    **Reset Type:** CPU Reset  
    **Comments:** See Chapter 13 Watchdog Timers (WDT)

**Footnotes:**
- Chip Reset can be triggered by the following three sources:
  - Triggered by chip power-on;
  - Triggered by brown-out detector;
  - Triggered by Super Watchdog (SWD).

2. Once brown-out status is detected, the detector will trigger System Reset or Chip Reset, depending on register configuration.

**Footer:**
- Page Number: 528
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems

**Navigation Links:**
- Submit Documentation Feedback