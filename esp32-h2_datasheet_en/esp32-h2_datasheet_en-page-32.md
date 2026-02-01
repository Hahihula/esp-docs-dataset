**Title: Functional Description**

---

### Section Title

#### Subsection (4.1.3.5) Event Task Matrix

The Event Task Matrix (ETM) allows events from any specified peripheral to be mapped to tasks of any specified peripheral, enabling peripherals to execute specified tasks without CPU intervention. Peripherals supporting ETM include GPIO, LED PWM, general-purpose timers, RTC Timer, system timer, MCPWM, temperature sensor, ADC, I2S, DMA, and PMU.

**Feature List**
- 50 channels that can be enabled and configured independently
- Receive 122 events from multiple peripherals
- Generate 129 tasks for multiple peripherals

For details, see [ESP32-H2 Technical Reference Manual > Chapter Event Task Matrix](#).

---

#### Subsection (4.1.3.6) Power Management Unit

The ESP32-H2 has an advanced Power Management Unit (PMU). It can be flexibly configured to power up different power domains of the chip to achieve the best balance between chip performance, power consumption, and wakeup latency.

Configuring the PMU is a complex procedure. To simplify power management for typical scenarios, there are the following predefined power modes that power up different combinations of power domains:

- **Active mode** – The CPU, RF circuits, and all peripherals are on. The chip can process data, receive, transmit, and listen.
  
- **Modem-sleep mode** – The CPU is on, but the clock frequency can be reduced. The wireless connections can be configured to remain active as RF circuits are periodically switched on when required.

- **Light-sleep mode** – The CPU stops running, and can be optionally powered on. The LP peripherals can be woken up periodically by the timer. The chip can be woken up via all wake-up mechanisms: Modem, RTC timer, or external interrupts. Wireless connections can remain active. Some groups of digital peripherals can be optionally powered off.

- **Deep-sleep mode** – Only LP system is powered on. Wireless connection data is stored in LP memory.

For power consumption in different power modes, see Section 5.5 Current Consumption.
For details, see [ESP32-H2 Technical Reference Manual > Chapter Low-Power Management](#).

---

#### Subsection (4.1.3.7) System Timer

The System Timer (SYSTIMER) in the ESP32-H2 chip is a 52-bit timer that can be used to generate tick interrupts for the operating system or as a general timer to generate periodic or one-time interrupts.

**Feature List**
- Two 52-bit counters and three 52-bit comparators
- 52-bit alarm values and 26-bit alarm periods

---

Espressif Systems  
32  
[Submit Documentation Feedback](#)  
ESP32-H2 Series Datasheet v1.2