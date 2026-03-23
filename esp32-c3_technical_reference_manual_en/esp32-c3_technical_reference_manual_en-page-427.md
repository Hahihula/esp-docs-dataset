

```markdown
Chapter 16 System Registers (SYSREG)
GoBack

Chapter 16

System Registers (SYSREG)

16.1 Overview

The ESP32-C3 integrates a large number of peripherals, and enables the control of individual peripherals to achieve optimal characteristics in performance-vs-power-consumption scenarios. Specifically, ESP32-C3 has various system configuration registers that can be used for the chip's clock management (clock gating), power management, and the configuration of peripherals and core-system modules. This chapter lists all these system registers and their functions.

16.2 Features

ESP32-C3 system registers can be used to control the following peripheral blocks and core modules:

* System and memory
* Clock
* Software Interrupt
* Low-power management
* Peripheral clock gating and reset

16.3 Function Description

16.3.1 System and Memory Registers

16.3.1.1 Internal Memory

The following registers can be used to control ESP32-C3's internal memory:

* In register SYSCON_CLKGATE_FORCE_ON_REG:
  - Setting different bits of the SYSCON_ROM_CLKGATE_FORCE_ON field forces on the clock gates of different blocks of Internal ROM 0 and Internal ROM 1.
  - Setting different bits of the SYSCON_SRAM_CLKGATE_FORCE_ON field forces on the clock gates of different blocks of Internal SRAM.
  - This means when the respective bits of this register are set to 1, the clock gate of the corresponding ROM or SRAM blocks will always be on. Otherwise, the clock gate will turn on automatically when the corresponding ROM or SRAM blocks are accessed and turn off
```