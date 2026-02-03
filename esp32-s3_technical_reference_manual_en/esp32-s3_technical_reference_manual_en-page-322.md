**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**GoBack Link:** [GoBack](#)

**Note Section:**
If more than 8 bits are requested, i.e., High - Low + 1 > 8, then the instruction will pad with zeros the bits above the eighth bit.

See notes regarding `addr_ulp` in Section **2.5.2.12**.

---

**Section Title:** 
2.6 ULP-RISC-V

**Subsection:**
2.6.1 Features
- Support RV32IMC instruction set
- Thirty-two 32-bit general-purpose registers
- 32-bit multiplier and divider
- Support for interrupts

**Subsection:**
2.6.2 Multiplier and Divider

ULP-RISC-V has an independent multiplication and division unit. The efficiency of multiplication and division instructions is shown in the following table.

**Table Title:** 
Table **2.6-1**: Instruction Efficiency

| Operation | Instruction | Execution Cycle | Instruction Description |
|-----------|-------------|------------------|-------------------------|
| Multiply  | MUL         | 34               | Multiply two 32-bit integers and return the lower 32-bit of the result |
|           | MULH        | 66               | Multiply two 32-bit signed integers and return the higher 32-bit of the result |
|           | MULHU       | 66               | Multiply two 32-bit unsigned integers and return the higher 32-bit of the result |
|           | MULHSU      | 66               | Multiply a 32-bit signed integer with an unsigned integer and return the higher 32-bit of the result |
|           | MULH30      | 66               | |

**Footer:**
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)