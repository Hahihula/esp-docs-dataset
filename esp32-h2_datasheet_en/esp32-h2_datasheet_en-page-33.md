**Title: Functional Description**

- Two modes to generate alarms: target mode and period mode

- Three comparators generating three independent interrupts based on configured alarm value or alarm period

- Ability to load back sleep time recorded by RTC timer via software after Deep-sleep or Light-sleep

- Counters can be stalled if the CPU is stalled or in OCD mode

- Real-time alarm events

For details, see [ESP32-H2 Technical Reference Manual > Chapter System Timer](#).

---

**Subtitle: 4.1.3.8 Timer Groups**

The Timer Group (TIMG) in the ESP32-H2 chip can be used to precisely time an interval, trigger an interrupt after a particular interval (periodically and aperiodically), or act as a hardware clock. ESP32-H2 has two timer groups, each consisting of one general-purpose timer and one Main System Watchdog Timer.

**Feature List**
- 16-bit prescaler
- 54-bit auto-reload-capable up-down counter
- Able to read real-time value of the time-base counter
- Halt, resume, and disable the time-base counter
- Programmable alarm generation
- Timer value reload (auto-reload at an alarm or a software-controlled instant reload)
- RTC slow clock frequency calculation
- Level interrupt generation
- Support for several ETM tasks and events

For details, see [ESP32-H2 Technical Reference Manual > Chapter Timer Group (TIMG)](#).

---

**Subtitle: 4.1.3.9 Watchdog Timers**

The Watchdog Timers (WDT) in ESP32-H2 are used to detect and recover from malfunctions. The chip contains three digital watchdog timers: one in each of the two timer groups (MWDT) and one in the RTC Module (RWDT). Additionally, there is one analog watchdog timer called the Super watchdog (SWD) that helps prevent the system from operating in a sub-optimal state.

**Feature List**
- Digital watchdog timers:
  - Four stages, each with separately programmable timeout value and timeout action
  - Timeout actions: Interrupt, CPU reset, core reset, system reset (RWDT only)
  - Flash boot protection under SPI Boot mode at stage O

Espressif Systems  
33  
[Submit Documentation Feedback](#)  
ESP32-H2 Series Datasheet v1.2