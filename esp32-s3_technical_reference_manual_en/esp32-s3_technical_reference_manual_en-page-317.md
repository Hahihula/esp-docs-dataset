**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Note Section:**
- This instruction can only access 32-bit memory words.
- The “Mem” loaded is the RTC_SLOW_MEM memory. Address O, as seen by the ULP coprocessor, corresponds to address 0x50000000, as seen by the main CPU.

**Section Title:**
2.5.2.4 JUMP – Jump to an Absolute Address

**Table Description (Figure 2.5-11): Instruction Type - JUMP**

| Type | Sel   | ImmAddr | Rdst |
|------|-------|---------|------|
|      |       |         |      |

**Table Content:**
- **Type:** [8, 1]
- **Sel:** [31 to 20]

**Figure Caption (Figure 2.5-11): Instruction Type - JUMP**

**Description Section for JUMP:**
- Operands:
  - Rdst: Register R[0-3], containing address to jump to (expressed in 32-bit words)
  - ImmAddr: 11-bit address, expressed in 32-bit words
  - Sel: Select the address to jump to.
    - O: jump to the address stored in ImmAddr
    - I: jump to the address stored in Rdst

- Jump type:
  - J: make an unconditional jump
  - Z: jump only if the last ALU operation has set zero flag
  - C: jump only if the last ALU operation has set overflow flag
  
**Note Section for JUMP:**
All jump addresses are expressed in 32-bit words.

**Section Title (continued): Description**

The instruction executes a jump to a specified address. The jump can be either unconditional or based on the ALU flag.

---

**Section Title:**
2.5.2.5 JUMPR – Jump to a Relative Address (Conditional upon RO)

**Table Description (Figure 2.5-12): Instruction Type - JUMPR**

| Sp   | Cond    | Threshold |
|------|---------|-----------|
|      |         |           |

**Table Content:**
- **Sp:** [31, 8]
- **Cond:** [0 to 7]
- **Threshold:** [0]

**Figure Caption (Figure 2.5-12): Instruction Type - JUMPR**

---

**Footer Information:**
Espressif Systems
Page number: 317
Document version and title: ESP32-S3 TRM (Version 1.7)
Feedback link text: Submit Documentation Feedback