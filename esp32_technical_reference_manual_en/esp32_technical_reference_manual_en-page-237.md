**Chapter Title:**
Chapter 12

**Section Titles and Content:**

- **DPort Registers**
  - **Subsection 12.1 Introduction**
    The ESP32 integrates a large number of peripherals, enabling the control of individual peripherals to achieve optimal characteristics in performance-vs-power-consumption scenarios. DPort registers manage clock gating (clock management), power management, and configuration of peripherals and core-system modules.

- **Subsection 12.2 Features**
  - DPort registers correspond to different peripheral blocks and core modules:
    - System and memory
    - Reset and clock
    - Interrupt matrix
    - DMA
    - MPU/MMU
    - APP_CPU controller
    - Peripheral clock gating and reset

- **Subsection 12.3 Functional Description**
  - **Sub-subsection 12.3.1 System and Memory Register**
    System and memory registers are used for system configuration, such as cache configuration and memory remapping.

  - **Sub-subsection 12.3.2 Reset and Clock Registers**
    Reset and clock registers can be found in Section 12.4 (Reset and clock registers). For more details about these registers refer to Chapter [Reset and Clock](#).

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)