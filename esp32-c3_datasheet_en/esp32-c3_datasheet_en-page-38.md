**Title: Functional Description**

---

### **4.1.3.5 System Timer**

ESP32-C3 integrates a 52-bit system timer, which has two 52-bit counters and three comparators. The system timer has the following features:

- counters with a fixed clock frequency of 16 MHz
- three types of independent interrupts generated according to alarm value
- two alarm modes: target mode and period mode
- 52-bit target alarm value and 26-bit periodic alarm value
- automatic reload of counter value
- counters can be stalled if the CPU is stalled or in OCD mode

For details, see [ESP32-C3 Technical Reference Manual > Chapter System Timer](#).

---

### **4.1.3.6 Power Management Unit**

The ESP32-C3 has an advanced Power Management Unit (PMU). It can be flexibly configured to power up different power domains of the chip to achieve the best balance between chip performance, power consumption, and wakeup latency.

Configuring the PMU is a complex procedure. To simplify power management for typical scenarios, there are the following predefined power modes that power up different combinations of power domains:

- **Active mode** – The CPU, RF circuits, and all peripherals are on. The chip can process data, receive, transmit, and listen.
  
- **Modem-sleep mode** – The CPU is on, but the clock frequency can be reduced. The wireless connections can be configured to remain active as RF circuits are periodically switched on when required.

- **Light-sleep mode** – The CPU stops running, and can be optionally powered on. The chip can be woken up via all wake up mechanisms: MAC, RTC timer, or external interrupts. Wireless connections can remain active. Some groups of digital peripherals can be optionally shut down.
  
- **Deep-sleep mode** – Only RTC is powered on. Wireless connection data is stored in RTC memory.

For power consumption in different power modes, see Section 5.6 Current Consumption.

Figure [4-2 Components and Power Domains](#) show the distribution of chip components between *power domains* and *power subdomains*. 

---

**Footer:**
Espressif Systems  
[Submit Documentation Feedback](#)  
ESP32-C3 Series Datasheet v2.2

Page 38