**Title: Functional Description**

- programmable alarm generation

- timer value reload (auto-reload at an alarm or a software-controlled instant reload)

- frequency calculation of slow clock for TIMGO

- level interrupt generation

- real-time alarm events

- support several ETM tasks and events

For details, see [ESP32-C5 Technical Reference Manual > Chapter Timer Group (TIMG)](#).

---

**Subtitle: 4.1.3.9 Watchdog Timers**

The Watchdog Timers (WDT) in ESP32-C5 are used to detect and recover from malfunctions. The chip contains three digital watchdog timers: one in each of the two timer groups (MWDT) and one in the RTC Module (RWDT). Additionally, there is one analog watchdog timer called the Super watchdog (SWD) that helps prevent the system from operating in a sub-optimal state.

**Feature List**

- **digital watchdog timers:**  
  - four stages, each with a programmable timeout value. Each stage can be configured, enabled and disabled separately

- three timeout actions for MWDT: interrupt, CPU reset, or core reset upon expiry of each stage; four timeout actions for RWDT interrupt: CPU reset, core reset, or system reset for RWDT upon expiry of each stage

- 32-bit expiry counter

- write protection, to prevent RWDT and MWDT configuration from being altered inadvertently

- flash boot protection  
  If the boot process from an SPI flash does not complete within a predetermined period of time, the watchdog will reboot the entire main system

- **analog watchdog timer:**  
  - ultra-low power
  - interrupt to indicate that the SWD is about to time out
  - various dedicated methods for software to feed SWD, which enables SWD to monitor the working state of the whole operating system

For details, see [ESP32-C5 Technical Reference Manual > Chapter Watchdog Timers](#).

---

**Subtitle: 4.1.3.10 RTC Timer**

ESP32-C5 RTC Timer is a 48-bit readable counter that can operate in any power mode. It is used as a system timer when the timers in the HP system is unavailable. It also allows for configuring timer interrupts and logging the time when specific events happen in the system.

---

**Footer:**
Espressif Systems  
[Submit Documentation Feedback](#)  
ESP32-C5 Series Datasheet v1.0

Page number 42