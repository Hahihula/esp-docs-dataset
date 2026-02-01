**Title: Functional Description**

- **4.1.3.10 Permission Control**
  The Permission Control module in ESP32-H2 is responsible for managing access permissions to memory and peripheral registers. It consists of two parts: PMP (Physical Memory Protection) and APM (Access Permission Management).

  - Feature List
    - Access permission management for ROM, HP memory, HP peripheral, LP memory, and LP peripheral address spaces.
    - APM supports each master (such as DMA) to select one of the four security modes.
    - Access permission configuration for up to 16 address ranges.

**4.1.3.11 System Registers**
The System Registers in the ESP32-H2 chip are used to configure various auxiliary chip features.

- Feature List
  - Control external memory encryption and decryption
  - Control Bus timeout protection

**4.1.3.12 Debug Assistant**
The Debug Assistant provides a set of functions to help locate bugs and issues during software debugging. It offers various monitoring capabilities and logging features to assist in identifying and resolving software errors efficiently.

- Feature List
  - Read/write monitoring: Monitor whether the CPU bus reads from or writes to a specified memory address space.
  - Stack pointer (SP) monitoring: Monitor whether the stack pointer is out of a limited range (overflows), and generates an interrupt if overflow occurs. violation will trigger an interrupt.

**Footer**
- Page number: 34
- Document title: ESP32-H2 Series Datasheet v1.2

**Navigation Links**
- Submit Documentation Feedback