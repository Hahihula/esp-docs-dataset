**4 Functional Description**

- Multiple interrupt sources mapping to a single CPU interrupt (i.e., shared interrupts)
For details, see [ESP32-C6 Technical Reference Manual > Chapter Interrupt Matrix](#).

---

**4.1.3.5 Event Task Matrix**

The Event Task Matrix (ETM) allows events from any specified peripheral to be mapped to tasks of any specified peripheral, enabling peripherals to execute specified tasks without CPU intervention. Peripherals supporting ETM include GPIO, LED PWM, general-purpose timers, RTC Timer, system timer, MCPWM, temperature sensor, ADC, I2S, LFP CPU, GDMA, and PMU.

**Feature List**
- 50 channels that can be enabled and configured independently
- Receive 124 events from multiple peripherals
- Generate 130 tasks for multiple peripherals

For details, see [ESP32-C6 Technical Reference Manual > Chapter Event Task Matrix](#).

---

**4.1.3.6 System Timer**

The System Timer (SYSTIMER) in the ESP32-C6 chip is a 52-bit timer that can be used to generate tick interrupts for the operating system or as a general timer to generate periodic or one-time interrupts.

**Feature List**
- Two 52-bit counters and three 52-bit comparators
- 52-bit alarm values and 26-bit alarm periods
- Two modes to generate alarms: target mode and period mode
- Three comparators generating three independent interrupts based on configured alarm value or alarm period
- Ability to load back sleep time recorded by RTC timer via software after Deep-sleep or Light-sleep
- Counters can be stalled if the CPU is stalled or in OCD mode
- Real-time alarm events

For details, see [ESP32-C6 Technical Reference Manual > Chapter System Timer](#).

---

**4.1.3.7 Power Management Unit**

The ESP32-C6 has an advanced Power Management Unit (PMU). It can be flexibly configured to power up different power domains of the chip to achieve the best balance between chip performance, power consumption, and wakeup latency.

The integrated LP CPU allow the ESP32-C6 to operate in Deep-sleep mode with most of the power domains turned off, thus achieving extremely low-power consumption. Configuring the PMU is a complex procedure. To simplify power management for typical scenarios, there are the following predefined power modes that power up different combinations of power domains:

- [ESP32-C6 Series Datasheet v1.4](#)

Espressif Systems

**Submit Documentation Feedback**

Page 43