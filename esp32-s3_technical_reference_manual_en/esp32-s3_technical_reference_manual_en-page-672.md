**Title:**
Chapter 13

**Subtitle:**
Watchdog Timers (WDT)

**Section Title:**
13.1 Overview

**Body Text:**
Watchdog timers are hardware timers used to detect and recover from malfunctions. They must be periodically fed (reset) to prevent a timeout. A system/software that is behaving unexpectedly (e.g., is stuck in a software loop or in overdue events) will fail to feed the watchdog thus trigger a watchdog timeout.

Therefore, watchdog timers are useful for detecting and handling erroneous system/software behavior.
As shown in Figure 13.1-1, ESP32-S3 contains three digital watchdog timers: one in each of the two timer groups in Chapter 12 Timer Group (TIMG) (called Main System Watchdog Timers, or MWDT) and one in the RTC Module (called the RTC Watchdog Timer, or RWDT). Each digital watchdog timer allows for four separately configurable stages and each stage can be programmed to take one action upon expiry, unless the watchdog is fed or disabled. MWDT supports three timeout actions: interrupt, CPU reset, core reset, while RWDT supports four timeout actions: interrupt, CPU reset, core reset, and system reset (see details in Section 13.2.2.2 Stages and Timeout Actions). A timeout value can be set for each stage individually.

During the flash boot process, RWDT and the first MWDT in timer group O are enabled automatically in order to detect and recover from booting errors.
ESP32-S3 also has one analog watchdog timer: Super watchdog (SWD). It is an ultra-low-power circuit in analog domain that helps to prevent the system from operating in a sub-optimal state and resets the system if required.

**Figure Caption:**
Figure 13.1-1. Watchdog Timers Overview

**Diagram Description:**
The diagram shows various components of ESP32-S3, including Main System Watchdog Timer (MWDT0), RTC Watchdog Timer RWDT in Digital Domain, and Super Watchdog SWD in Analog Domain.

**Footer Texts:**
Espressif Systems
672
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Navigation Link:**
GoBack