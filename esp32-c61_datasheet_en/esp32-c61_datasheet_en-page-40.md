**Title: Functional Description**

---

### **4.1.3.11 Watchdog Timers**

The Watchdog Timers (WDT) in ESP32-C61 are used to detect and recover from malfunctions. The chip contains three digital watchdog timers: one in each of the two timer groups (MWDT) and one in the RTC Module (RWDT). Additionally, there is one analog watchdog timer called the Super watchdog (SWD) that helps prevent the system from operating in a sub-optimal state.

**Feature List**
- Digital watchdog timers:
  - Four stages, each with a separately programmable timeout value and timeout action
  - Timeout actions: Interrupt, CPU reset, core reset, system reset (RWDT only)
  - Flash boot protection under SPI Boot mode at stage O
  - Write protection that makes WDT register read-only unless unlocked
  - 32-bit timeout counter

- Analog watchdog timer:
  - Timeout period slightly less than one second
  - Timeout actions: Interrupt, system reset

---

### **4.1.3.12 Permission Control**

The Permission Control module in ESP32-C61 is responsible for managing access permissions to memory and peripheral registers. It consists of two parts: PMP (Physical Memory Protection) and APM (Access Permission Management).

**Feature List**
- Access permission management for ROM, HP memory, HP peripheral, and LP peripheral address spaces
- APM supports each master (such as DMA) to select one of the four security modes
- Access permission configuration for up to 16 address ranges
- Interrupt function and exception information record

---

### **4.1.3.13 System Registers**

The System Registers in the ESP32-C61 chip are used to configure various auxiliary chip features.

**Feature List**
- Control External memory encryption and decryption
- Control CPU core debugging
- Control Bus timeout protection

---

*Espressif Systems*
*ESP32-C61 Series Datasheet v0.5*

Page 40