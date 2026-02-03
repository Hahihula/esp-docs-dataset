**Chapter Title:**
Chapter 17 System Registers (SYSTEM)

**GoBack Link:** [GoBack](#)

---

### Chapter Overview

#### Section Heading:
17.1 **Overview**

**Body Text:**
The ESP32-S3 integrates a large number of peripherals, and enables the control of individual peripherals to achieve optimal characteristics in performance-vs-power-consumption scenarios. Specifically, ESP32-S3 has a various of system configuration registers that can be used for the chip’s clock management (clock gating), power management, and the configuration of peripherals and core-system modules. This chapter lists all these system registers and their functions.

#### Section Heading:
17.2 **Features**

**Body Text:**
ESP32-S3 system registers can be used to control the following peripheral blocks and core modules:

- System and memory
- Clock
- Software Interrupt
- Low-power management
- Peripheral clock gating and reset
- CPU Control

---

### Function Description Section

#### Subsection Heading:
17.3 **Function Description**

#### Sub-subsection Heading: 
17.3.1 Internal Memory

**Sub-subsection Text:**
The following registers can be used to control ESP32-S3’s internal memory:

- In register SYSCON_CLKGATE FORCE ON REG:
  - Setting different bits of the SYSCON_ROM_CLKGATE FORCE ON field forces on the clock gates of different blocks of Internal ROM O and Internal ROM 1.
  - Setting different bits of the SYSCON_SRAM_CLKGATE FORCE ON field forces on the clock gates of different blocks of Internal SRAM.

- This means when the respective bits of this register are set to 1, the clock gate of the corresponding ROM or SRAM blocks will always be on. Otherwise, the clock gate will turn off these memory banks and they become inaccessible until reset by software (by setting all relevant bits back).

---

**Footer:**
Espressif Systems  
Page Number: 822  
Document Title: ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback Link