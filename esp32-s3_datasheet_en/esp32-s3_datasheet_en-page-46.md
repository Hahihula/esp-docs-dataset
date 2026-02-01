**Title: Functional Description**

- Upon expiry of each stage:
  - Interrupt, CPU reset, or core reset occurs for MWDT (Multi-Watchdog Timer)
  - Interrupt, CPU reset, core reset, or system reset occurs for RWDT (Real-time Watchdog Timer)

- **32-bit expiry counter**
  
- Write protection: to prevent RWDT and MWDT configuration from being altered inadvertently
  
- Flash boot protection: If the boot process from an SPI flash does not complete within a predetermined period of time, the watchdog will reboot the entire main system

**For details, see ESP32-S3 Technical Reference Manual > Chapter Watchdog Timers.**

---

**Subtitle: 4.1.3.9 XTAL32K Watchdog Timers**

**Sub-subtitle: Interrupt and Wake-Up**
  
When the XTAL32K watchdog timer detects the oscillation failure of XTAL32K_CLK, an oscillation failure interrupt RTC_XTAL32K DEAD_IN (for interrupt description, please refer to ESP32-S3 Technical Reference Manual > Chapter Low-power Management) is generated. At this point, the CPU will be woken up if in Light-sleep mode or Deep-sleep mode.

**Sub-subtitle: BACKUP32K_CLK**

Once the XTAL32K watchdog timer detects the oscillation failure of XTAL32K_CLK, it replaces XTAL32K_CLK with BACKUP32K_CLK (with a frequency of 32 kHz or so) derived from RTC_CLK as RTC’s SLOW_CLK, so to ensure proper functioning of the system.

**For details, see ESP32-S3 Technical Reference Manual > Chapter XTAL32K Watchdog Timers.**

---

**Subtitle: 4.1.3.10 Permission Control**

In ESP32-S3, the Permission Control module is used to control access to the slaves (including internal memory, peripherals, external flash, and RAM). The host can access its slave only if it has the right permission.

In this way, data and instructions are protected from illegitimate read or write. 

The ESP32-S3 CPU can run in both Secure World and Non-secure World where independent permission controls are adopted. The Permission Control module is able to identify which World the host is running and then proceed with its normal operations.

**Feature List**
- Manage access to internal memory by:
  - CPU
  - CPU trace module
  - GDMA
  
- Manage access to external flash and RAM by:
  - MMU
  - SPI1

---

Espressif Systems  
46 ESP32-S3 Series Datasheet v2.1  

[Submit Documentation Feedback](#)