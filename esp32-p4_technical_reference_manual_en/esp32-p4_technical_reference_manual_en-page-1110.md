

# Chapter 17
## Watchdog Timers (WDT)

### 17.1 Overview

Watchdog timers are hardware timers used to detect and recover from malfunctions. They must be periodically fed (reset) to prevent a timeout. A system/software that is behaving unexpectedly (e.g., is stuck in a software loop or in overdue events) will fail to feed the watchdog, thus the watchdog timer will time out and trigger an interrupt or reset, directing the system to a known state for exception handling or a restart. Therefore, watchdog timers are useful for detecting and handling erroneous system/software behavior.

As shown in Figure 17.1-1, ESP32-P4 contains three digital watchdog timers: one in each of the two timer groups in Chapter 16 Timer Group (TIMG) (called Main System Watchdog Timers, or MWDT) and one in the LP system (called the RTC Watchdog Timer, or RWDT). Each digital watchdog timer allows for four separately configurable stages, and each stage can be programmed to take one action upon timeout, unless the watchdog is fed or disabled. MWDT supports three timeout actions: interrupt, HP CPU reset, and HP core reset, while RWDT supports four timeout actions: interrupt, HP CPU reset, HP core reset, and system reset (see details in Section 17.2.2.2 Stages and Timeout Actions). A timeout value can be set for each stage individually.

In SPI Boot mode, RWDT and the MWDT in timer group 0 are enabled automatically in order to detect errors that may occur during the flash boot process and facilitate recovery.

ESP32-P4 also has one analog watchdog timer: Super watchdog (SWD). It is an ultra-low-power circuit in analog domain that helps to prevent the system from operating in a sub-optimal state and resets the system if required.

Figure 17.1-1. Watchdog Timers Overview

Espressif Systems
Submit Documentation Feedback
ESP32-P4 TRM
PRELIMINARY