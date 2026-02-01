**Title: Functional Description**

- **4.1.4.8 Timer Group (TIMG)**
  - ESP32-P4 chip contains two timer groups. Each timer group consists of two general-purpose timers and one Main System Watchdog Timer (MWDT). The general-purpose timer is based on a 16-bit prescaler and a 54-bit auto-reload-capable up-down counter.

    **Feature List**
    - A 54-bit time-base counter programmable to incrementing or decrementing
    - Three clock sources: PLL_F80M_CLK or XTAL_CLK or RC_FAST_CLK
    - A 16-bit clock prescaler, from 2 to 65536
    - Able to read real-time value of the time-base counter
    - Able to halt and resume the time-base counter
    - Programmable alarm generation
    - Timer value reload — Auto-reload at alarm or software-controlled instant reload
    - Calculate clock frequency — Calculate the measured frequency of the clock based on the crystal clock
    - Level interrupt generation
    - Support several ETM tasks and events

- **4.1.4.9 Watchdog Timers (WDT)**
  - ESP32-P4 contains three digital watchdog timers: one in each of the two timer groups (called Main System Watchdog Timers, or MWDT), and one in the LP system (called the RTC Watchdog Timer, or RWDT).
  - In SPI Boot mode, RWDT and the MWDT in timer group 0 are enabled automatically in order to detect errors that may occur during the flash boot process and facilitate recovery.
  - ESP32-P4 also has one analog watchdog timer: Super watchdog (SWD). It is an ultra-low-power circuit in analog domain that helps to prevent the system from operating in a sub-optimal state and resets the system if required.

    **Feature List**
    - Four stages, each with a separately programmable timeout value and timeout action
    - Timeout actions:
      - MWDT: interrupt, HP CPU reset, HP core reset
      - RWDT: interrupt, HP CPU reset, HP core reset, system reset
    - Flash boot protection under SPI Boot mode at stage 0:

**Footer**
- Espresso Systems
- Page number: 48
- Document title: ESP32-P4 Series Datasheet v0.6

**Link:** Submit Documentation Feedback