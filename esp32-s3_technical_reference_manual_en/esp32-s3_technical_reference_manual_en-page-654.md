**Chapter Title:**
Chapter 12 Timer Group (TIMG)

**GoBack Link:** GoBack

---

**Section Heading:**
12.1 Overview

**Body Text:**
General purpose timers can be used to precisely time an interval, trigger an interrupt after a particular interval (periodically and aperiodically), or act as a hardware clock. As shown in Figure 12.1-1, the ESP32-S3 chip contains two timer groups, namely timer group 0 and timer group 1. Each timer group consists of two general purpose timers referred to as Tx (where x is 0 or 1) and one Main System Watchdog Timer. All general purpose timers are based on 16-bit prescalers and 54-bit auto-reload-capable up-down counters.

**Figure Description:**
- **Title:** Figure 12.1-1. Timer Units within Groups
- Two diagrams labeled "Timer Group 0" with components:
  - Timer 0 (T0)
  - Timer 1 (T1)
  - Watchdog Timer (WDT)

- Another diagram for "Timer Group 1":
  - Timer 0 (T0)
  - Timer 1 (T1)
  - Watchdog Timer (WDT)

**Note:**
While the Main System Watchdog Timer registers are described in this chapter, their functional description is included in Chapter 13 Watchdog Timers (WDT). Therefore, the term 'timers' within this chapter refers to the general purpose timers.

The timers’ features are summarized as follows:
- A 16-bit clock prescaler, from 2 to 65536
- A 54-bit time-base counter programmable to incrementing or decrementing
- Able to read real-time value of the time-base counter
- Halting and resuming the time-base counter
- Programmable alarm generation
- Timer value reload (Auto-reload at alarm or software-controlled instant reload)
- Level interrupt generation

**Footer:**
Espressif Systems  
654 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback