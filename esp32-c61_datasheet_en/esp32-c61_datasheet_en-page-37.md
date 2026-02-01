**Title: Functional Description**

- **4.1.3.6 System Timer**
  
  The System Timer (SYSTIMER) in the ESP32-C61 chip is a 52-bit timer that can be used to generate tick interrupts for the operating system or as a general timer to generate periodic or one-time interrupts.

  - Feature List:
    - Two 52-bit counters and three 52-bit comparators
    - 52-bit alarm values and 26-bit alarm periods
    - Two modes to generate alarms: target mode and period mode
    - Three comparators generating three independent interrupts based on configured alarm value or alarm period
    - Ability to load back sleep time recorded by RTC timer via software after Deep-sleep or Light-sleep
    - Counters can be stalled if the CPU is stalled or in OCD mode
    - Real-time alarm events

- **4.1.3.7 Power Management Unit**

  The ESP32-C61 has an advanced Power Management Unit (PMU). It can be flexibly configured to power up different power domains of the chip to achieve the best balance between chip performance, power consumption, and wakeup latency.

  Configuring the PMU is a complex procedure. To simplify power management for typical scenarios, there are the following predefined power modes that power up different combinations of power domains:

  - Active mode – The CPU, RF circuits, and all peripherals are on. The chip can process data, receive, transmit, and listen.
  - Modem-sleep mode – The CPU is on, but the clock frequency can be reduced. The wireless connections can be configured to remain active as RF circuits are periodically switched on when required.
  - Light-sleep mode – The CPU stops running, and can be optionally powered on. The chip can be woken up via all wake up mechanisms: MAC, host, RTC timer, or external interrupts. Wireless connections can remain active. Some groups of digital peripherals can be optionally powered off.
  - Deep-sleep mode – Only LP system is powered on.

**Figure References**
- Figure 4-2 Components and Power Domains
- the following Figure 4-3 Components and Power Domains Table show the distribution of chip components between power domains and power subdomains. 

**Footer:**
Espressif Systems  
ESP32-C61 Series Datasheet v0.5

Page Number:
37