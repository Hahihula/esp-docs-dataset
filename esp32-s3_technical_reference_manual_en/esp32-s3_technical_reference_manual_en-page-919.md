**Title:**
Chapter 24 Clock Glitch Detection

**GoBack Link:** (Located at top right corner)

---

### Chapter Overview:
#### Section Title: **24.1 Overview**

The Clock Glitch Detection module on ESP32-S3 detects glitches in external crystal XTAL_CLK signals, and generates a system reset signal when detecting glitches to reset the whole digital circuit including RTC. By doing so, it prevents attackers from injecting glitches on external crystal XTAL_CLK clock to compromise ESP32-S3 and thus strengthens chip security.

---

### Functional Description:
#### Section Title: **24.2 Functional Description**

#### Subsection 1 (Title): 
**24.2.1 Clock Glitch Detection**

The Clock Glitch Detection module monitors input clock signals from XTAL_CLK for glitches, specifically a glitch is detected if it's less than or equal to three nanoseconds in width and the signal comes after an initial pulse of at least one nanosecond.

#### Subsection 2 (Title): 
**24.2.2 Reset**

Once detecting a glitch on XTAL_CLK that affects normal operation, this module triggers system reset if RTC_CNTL_GLITCH_RST_EN bit is enabled by default to enable the reset function.
  
---

**Figure Caption:**
Figure 24.2-1. XTAL_CLK Pulse Width

**Diagram Description:** 
The diagram shows two pulse widths labeled as 'a' and 'b', with a note indicating that these are related to clock glitch detection on ESP32-S3.

---

**Footer Information:**
Espressif Systems  
919  
Submit Documentation Feedback  
ESP32-S3 TRM (Version 1.7)