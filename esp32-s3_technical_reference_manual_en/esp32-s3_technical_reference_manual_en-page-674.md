**Title:**
Chapter 13 Watchdog Timers (WDT)

**Subtitle:**
GoBack

**Section Title:**
13.2 Digital Watchdog Timers

**Subsection Title and Content:**
13.2.1 Features

Watchdog timers have the following features:

- Four stages, each with a programmable timeout value. Each stage can be configured and enabled/disabled separately
- Three timeout actions (interrupt, CPU reset, or core reset) for MWDT and four timeout actions (interrupt, CPU reset, core reset, or system reset) for RWDT upon expiry of each stage
- 32-bit expiry counter
- Write protection, to prevent RWDT and MWDT configuration from being altered inadvertently
- Flash boot protection

If the boot process from an SPI flash does not complete within a predetermined period of time, the watchdog will reboot the entire main system.

**Footer:**
Espressif Systems  
674 ESP32-S3 TRM (Version 1.7)  

Submit Documentation Feedback