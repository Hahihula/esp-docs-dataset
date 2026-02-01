**Title: Functional Description**

---

**Subtitle: Power Management Unit (PMU)**

ESP32-S3 has an advanced Power Management Unit (PMU). It can be flexibly configured to power up different power domains of the chip to achieve the best balance between chip performance, power consumption, and wakeup latency.

The integrated Ultra-Low-Power (ULP) coprocessors allow ESP32-S3 to operate in Deep-sleep mode with most of the power domains turned off, thus achieving extremely low-power consumption. Configuring the PMU is a complex procedure. To simplify power management for typical scenarios, there are the following predefined **power modes** that power up different combinations of power domains:

- Active mode – The CPU, RF circuits, and all peripherals are on. The chip can process data, receive, transmit, and listen.
  
- Modem-sleep mode – The CPU is on, but the clock frequency can be reduced. The wireless connections can be configured to remain active as RF circuits are periodically switched on when required.

- Light-sleep mode – The CPU stops running, and can be optionally powered on. The RTC peripherals, as well as the ULP coprocessor can be woken up periodically by the timer. The chip can be woken up via all wake up mechanisms: MAC, RTC timer, or external interrupts. Wireless connections can remain active. Some groups of digital peripherals can be optionally powered off.

- Deep-sleep mode – Only RTC is powered on. Wireless connection data is stored in RTC memory.

For power consumption in different power modes, see Section 5.6 Current Consumption.

Figure A-2 Components and Power Domains and the following Table 4-1 show the distribution of chip components between **power domains** and **power subdomains**.

---

**Footer:**
Espressif Systems
ESP32-S3 Series Datasheet v2.1

Submit Documentation Feedback