**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Table of Instructions and Execution Cycles for Divide Operations**

| Operation | Instruction | Execution Cycle |
|-----------|-------------|------------------|
|           | DIV         | 34               |
|           | DIVU        | 34               |
| **Divide** | REM         | 34               |
|           | REMU        | 34               |

- **Instruction Description:**
  - Divide a 32-bit integer by a 32-bit integer and return the quotient.
  - Divide a 32-bit unsigned integer by a 32-bit unsigned integer and return the quotient
  - Divide a 32-bit signed integer by a 32-bit signed integer and return the remainder

**Section Title:**
2.6.3 ULP-RISC-V Interrupts

**Subsection Titles with Content:**

- **2.6.3.1 Introduction:** 
  The interrupt controller of ULP-RISC-V is implemented using a customized instruction set, instead of RISC-V Privileged ISA specification, aiming to reduce the size of ULP-RISC-V.

- **2.6.3.2 Interrupt Controller:**
  - "ULP-RISC-V has 32 interrupt sources but only four are available in real design as shown below."
  - Internal sources (INT0 ~ INT2) triggered by internal interrupt events.
  - External source (INT31, triggered by the peripheral interrupts of ESP32-S3).

**Table Title:**
Table 2.6-2. ULP-RISC-V Interrupt Sources

| Type | IRQ   | Triggered by                |
|------|-------|----------------------------|
|      |       | Internal timer interrupt    |
|      | 0     | Internal timer interrupt    |
|      | 1     | EBREAK/ECALL or Illegal Instruction |
|      | 2     | BUS Error (Unaligned Memory Access) |
|      | 31    | RTC peripheral interrupts   |

**Note:**
- "If illegal instruction interrupt or bus error interrupt is disabled, ULP-RISC-V goes to HALT when the two errors occur."
- "ULP-RISC-V provides four 32-bit interrupt registers (Q0 ~ Q3) to handle interrupt service routine (ISR). Table 2.6-3 shows the function of each register."

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version Information:**  
ESP32-S3 TRM (Version 1.7)

**Page Numbering and Navigation:**
GoBack
323