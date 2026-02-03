**Chapter Title:**
Chapter 14

**Subheading and Section Titles:**
XTAL32K Watchdog Timers (XTWDT)

**Section 14.1 Overview**

The XTAL32K watchdog timer on ESP32-S3 is used to monitor the status of external crystal XTAL32K_CLK. This watchdog timer can detect the oscillation failure of XTAL32K_CLK, change the clock source of RTC, etc.

When XTAL32K_CLK works as the clock source of RTC_SLOW_CLK (for clock description, see Chapter 7 Reset and Clock) and stops oscillating, the XTAL32K watchdog timer first switches to BACKUP32K_CLK derived from RC_SLOW_CLK and generates an interrupt (if the chip is in Light-sleep or Deep-sleep mode, the CPU will be woken up), then switches back to XTAL32K_CLK after it is restarted by software.

**Figure Description:**
Figure 14.1-1 shows a block diagram of XTLA32K Watchdog Timer with connections labeled as:
- XTAL32K_CLK
- RTC_SLOW_CLK
- BACKUP32K_CLK_EN (Monitor)
- RTC_CNTL_XTAL32K_WDT_EN
- Interrupt

**Section 14.2 Features**

**Subsection Title:**
14.2.1 Interrupt and Wake-Up

When the XTAL32K watchdog timer detects the oscillation failure of XTAL32K_CLK, an oscillation failure interrupt RTC_XTAL32K_DEAD_INT (for interrupt description, please refer to Chapter 10 Low-power Management [RTC_CNTL]) is generated. At this point, the CPU will be woken up if in Light-sleep mode or Deep-sleep mode.

**Footer:**
Espressif Systems
680 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback