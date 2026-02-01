**Title: Functional Description**

- **Active mode**: The HP CPU, RF circuits, and all peripherals are on. The chip can process data, receive, transmit, and listen.
  
- **Modem-sleep mode**: The HP CPU is on, but the clock frequency can be reduced. The wireless connections can be configured to remain active as RF circuits are periodically switched on when required.

- **Light-sleep mode**: The HP CPU stops running, and can be optionally powered on. The LP peripherals, as well as the LP CPU can be woken up periodically by the timer. The chip can be woken up via all wake up mechanisms: MAC, SDIO host, RTC timer, or external interrupts. Wireless connections can remain active. Some groups of digital peripherals can be optionally powered off.

- **Deep-sleep mode**: Only the LP system is powered on. Wireless connection data is stored in LP memory.
  
For modules powered on in each power mode, see Figure ESP32-C6 Functional Block Diagram.

For power consumption in different power modes, see Section 5.6 Current Consumption

**Characteristics:**

For details, see ESP32-C6 Technical Reference Manual > Chapter Low-Power Management.

---

**4.1.3.8 Timer Group**

The Timer Group (TIMG) in the ESP32-C6 chip can be used to precisely time an interval, trigger an interrupt after a particular interval (periodically and aperiodically), or act as a hardware clock. ESP32-C6 has two timer groups, each consisting of one general-purpose timer and one Main System Watchdog Timer.

**Feature List**

- 16-bit prescaler
- 54-bit auto-reload-capable up-down counter
- Able to read real-time value of the time-base counter
- Halt, resume, and disable the time-base counter
- Programmable alarm generation
- Timer value reload (auto-reload at an alarm or a software-controlled instant reload)
- RTC slow clock frequency calculation
- Real-time alarm events
- Level interrupt generation
- Support for several ETM tasks and events

For details, see ESP32-C6 Technical Reference Manual > Chapter Timer Group (TIMG).

---

**4.1.3.9 Watchdog Timers**

The Watchdog Timers (WDT) in ESP32-C6 are used to detect and recover from malfunctions. The chip contains three digital watchdog timers: one in each of the two timer groups (MWDT) and one in the RTC Module (RWDT). Additionally, there is one analog watchdog timer called the Super watchdog (SWD) that helps prevent the system from operating in a sub-optimal state.

Espressif Systems

44
Submit Documentation Feedback