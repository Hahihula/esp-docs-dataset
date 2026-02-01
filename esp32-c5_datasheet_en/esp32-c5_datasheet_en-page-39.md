**Title: Functional Description**

---

### **4.1.3.2 Reset**

The ESP32-C5 chip provides four types of reset that occur at different levels, namely CPU Reset, Core Reset, System Reset, and Chip Reset. Except for Chip Reset, all reset types preserve the data stored in internal memory.

**Feature List**
- Four types of reset:
  - **CPU reset**: resets the CPU core
  - **core reset**: resets the whole digital system except for the LP system
  - **system Reset**: resets the whole digital system, including the LP system
  - **chip reset**: resets the whole chip

**reset trigger:**
- directly by hardware
- via software by configuring the corresponding registers of the CPU
- support for retrieving reset cause

For details, see [ESP32-C5 Technical Reference Manual > Chapter Reset and Clock](#).

---

### **4.1.3.3 Clock**

The ESP32-C5 chip has clocks sourced from oscillators, RC circuits, and PLL circuits, which are then processed by dividers or selectors. The clocks can be classified into high-speed clocks for devices working at higher frequencies and slow-speed clocks for low-power systems and some peripherals.

**Feature List**
- **high-speed clocks for HP system**
  - external main crystal clock (supports 48 MHz crystal clock frequency)
  - internal fast RC oscillator clock (typically about 20 MHz, and adjustable)
  - PLL clock
- **slow-speed clocks for RTC counter, RTC watchdog, and the power management unit (PMU)**
  - internal slow RC oscillator (typically about 150 kHz)
  - 32 kHz external low-speed crystal clock
  - external IO clock (external clock source connected with digital IO)

**Notice:**
- ESP32-C5 is unable to operate without an external main crystal clock.
- ESP32-C5 can automatically filter out high-frequency glitches from the external main crystal clock.

---

Espressif Systems  
[Submit Documentation Feedback](#)  
ESP32-C5 Series Datasheet v1.0

**Page Number: 39**