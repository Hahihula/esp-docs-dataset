**Title: Functional Description**

---

### **4.1.4.5 True Random Number Generator**

The ESP32-C61 contains a true random number generator, which generates 32-bit random numbers that can be used for cryptographical operations, among other things.

The true random number generator in ESP32-C61 generates true random numbers, which means random numbers generated from a physical process, rather than by means of an algorithm. No number generated within the specified range is more or less likely to appear than any other number.

**Feature List**
- RNG entropy source
  - Thermal noise from high-speed ADC or SAR ADC
  - An asynchronous clock mismatch

---

### **4.1.4.6 Power Glitch Detector**

ESP32-C61 can monitor the voltage of the power supply in real time. When a voltage glitch occurs, the chip will reset immediately to prevent power glitch attacks.

**Feature List**
- Configurable threshold for power glitch (around 2.7 V by default)
- Enabled upon power-up

---

*Espressif Systems*
*ESP32-C61 Series Datasheet v0.5*

Page number: **43**