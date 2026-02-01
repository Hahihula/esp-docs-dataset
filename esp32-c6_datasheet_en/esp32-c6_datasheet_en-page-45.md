Title: Functional Description

Subtitle: Feature List

- Digital watchdog timers:
  - Four stages, each with a separately programmable timeout value and timeout action
  - Timeout actions: Interrupt, CPU reset, core reset, system reset (RWDT only)
  - Flash boot protection under SPI Boot mode at stage 0
  - Write protection that makes WDT register read-only unless unlocked
  - 32-bit timeout counter

- Analog watchdog timer:
  - Timeout period slightly less than one second
  - Timeout actions: Interrupt, system reset

For details, see [ESP32-C6 Technical Reference Manual > Chapter Watchdog Timers](#).

---

Subtitle: Permission Control (4.1.3.10)

Body Text:

The Permission Control module in ESP32-C6 is responsible for managing access permissions to memory and peripheral registers. It consists of two parts: PMP (Physical Memory Protection) and APM (Access Permission Management).

Feature List

- Access permission management for ROM, HP memory, HP peripheral, LP memory, and LP peripheral address spaces
- APM supports each master (such as DMA) to select one of the four security modes
- Access permission configuration for up to 16 address ranges
- Interrupt function and exception information record

For details, see [ESP32-C6 Technical Reference Manual > Chapter Permission Control (PMS)](#).

---

Subtitle: System Registers (4.1.3.11)

Body Text:

The System Registers in the ESP32-C6 chip are used to configure various auxiliary chip features.

Feature List

- Control External memory encryption and decryption
- Control HP core/LP core debugging
- Control Bus timeout protection

For details, see [ESP32-C6 Technical Reference Manual > Chapter System Registers (HP_SYSREG)](#).

---

Footer:
Espressif Systems
45
Submit Documentation Feedback ESP32-C6 Series Datasheet v1.4