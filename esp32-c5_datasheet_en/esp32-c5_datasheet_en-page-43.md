**Title: Functional Description**

---

### Feature List

- **48-bit counter operating under the RTC clock**
- real-time reading of the time-base counter’s value
- configurable target value for the counter to trigger an interrupt upon timeout

For details, see [ESP32-C5 Technical Reference Manual](#) > Chapter RTC Timer.

---

**Subtitle: 4.1.3.11 Permission Control**

The Permission Control module in ESP32-C5 is responsible for managing access permissions to memory and peripheral registers. It consists of two parts: PMP (Physical Memory Protection) and APM (Access Permission Management).

### Feature List

- access permission management for ROM, HP memory, HP peripheral, and LP peripheral address spaces
- APM supports each master (such as DMA) to select one of the four security modes
- access permission configuration for up to 32 address ranges
- individual permission configuration for each register
- Interrupt function and exception information record

For details, see [ESP32-C5 Technical Reference Manual](#) > Chapter Permission Control (PMS).

---

**Subtitle: 4.1.3.12 System Registers**

The System Registers in the ESP32-C5 chip are used to configure various auxiliary chip features.

### Feature List

- control External memory encryption and decryption
- control CPU core debugging
- control Bus timeout protection

For details, see [ESP32-C5 Technical Reference Manual](#) > Chapter System Registers (HPSYSREG).

---

**Subtitle: 4.1.3.13 Debug Assistant**

The Debug Assistant provides a set of functions to help locate bugs and issues during software debugging. It offers various monitoring capabilities and logging features to assist in identifying and resolving software errors efficiently.

### Feature List

- read/write monitoring: Monitor whether the CPU bus reads from or writes to a specified memory address space

---

**Footer**

Espressif Systems  
[Submit Documentation Feedback](#) ESP32-C5 Series Datasheet v1.0