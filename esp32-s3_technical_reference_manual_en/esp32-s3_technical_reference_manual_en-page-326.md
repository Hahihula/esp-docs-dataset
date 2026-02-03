**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Figure Caption and Description:**
- **Figure 2.6-5. Interrupt Instruction — Maskirq rd rs**

**Table of Instructions:**
- **Operand | Description - See Figure 2.6-5**
  - `rd` : Target general purpose register, stores current value of register Q1.
  - `rs` : Source general purpose register, stores the value to be written to Q1.
  - `f7` : Interrupt instruction number.

**Subsection Title:**
2.6.3.5 RTC Peripheral Interrupts

**Body Text:**
The interrupts from some sensors, software, and RTC I2C can be routed to ULP-RISC-V. To enable the interrupts, please set the register SENS_SAR_COCPU_INT_ENA_REG , see Table 2.6-4.

**Footer Information:**
Espressif Systems
326 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback