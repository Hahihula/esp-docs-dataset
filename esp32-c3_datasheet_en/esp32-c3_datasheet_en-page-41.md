**4 Functional Description**

- Interrupt to indicate that the SWD timeout period is close to expiring

- Various dedicated methods for software to feed SWD, which enables SWD to monitor the working state of the whole operating system

---

**4.1.3.9 Permission Control**

ESP32-C3 includes a Permission Controller (PMS), which allocates the hardware resources (memory and peripherals) to two isolated environments, thereby realizing the separation of privileged and unprivileged environments.

- **Feature List**
  - Independent access management in a privileged environment and unprivileged environment
  - Independent access management to internal memory, including:
    - CPU access to internal memory
    - GDMA access to internal memory
  - Independent access management to external memory, including:
    - CPU to external memory via SPI1
    - CPU to external memory via Cache
  - Independent access management to peripheral regions, including:
    - CPU access to peripheral regions
    - Interrupt upon unsupported access alignment

- Address splitting for more flexible access management
- Register locks to secure the integrity of access management related registers
- Interrupt upon unauthorized access

For details, see [ESP32-C3 Technical Reference Manual > Chapter Permission Control (PMS)](#).

---

**4.1.3.10 System Registers**

The System Registers in the ESP32-C3 chip are used to configure various auxiliary chip features.

- **Feature List**
  - Control system and memory
  - Control clock
  - Control software interrupt
  - Control low-power management
  - Control peripheral clock gating and reset

For details, see [ESP32-C3 Technical Reference Manual > Chapter System Registers (HP_SYSREG)](#).

---

Espressif Systems  
41  
[Submit Documentation Feedback](#)  
ESP32-C3 Series Datasheet v2.2