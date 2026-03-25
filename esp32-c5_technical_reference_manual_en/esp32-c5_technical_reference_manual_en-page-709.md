

# Chapter 16

## Watchdog Timers (WDT)

### 16.1 Overview

Watchdog timers are hardware timers used to detect and recover from malfunctions. They must be periodically fed (reset) to prevent a timeout. A system/software that is behaving unexpectedly (e.g. is stuck in a software loop or in overdue events) will fail to feed the watchdog and thus trigger a watchdog timeout. Therefore, watchdog timers are useful for detecting and handling erroneous system/software behaviors.

As shown in Figure 16.1-1, ESP32-C5 contains three digital watchdog timers: one in each of the two timer groups in Chapter 15 Timer Group (TIMG) (called Main System Watchdog Timers, or MWDT) and one in the RTC Module (called the RTC Watchdog Timer, or RWDT). Each digital watchdog timer allows for four separately configurable stages and each stage can be programmed to take one action upon timeout, unless the watchdog is fed or disabled. MWDT supports three timeout actions: interrupt, CPU reset, and core reset, while RWDT supports four timeout actions: interrupt, CPU reset, core reset, and system reset (see details in Section 16.2.2.2 Stages and Timeout Actions). A timeout value can be set for each stage individually.

During the flash boot process, RWT and the MWDT in timer group 0 are enabled automatically in order to detect and recover from booting errors.

ESP32-C5 also has one analog watchdog timer: Super watchdog (SWD). It is an ultra-low-power circuit in analog domain that helps to prevent the system from operating in a sub-optimal state and resets the system if required.

Figure 16.1-1. Watchdog Timers Overview

```
Main System
Watchdog Timer 0 MWDT0          Main System
                                    Watchdog Timer 1
                                        MWDT1
RTC                                  Digital Domain
Watchdog Timer RWDT
Super Watchdog SWD                    Analog Domain
```