**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**GoBack Link:** [GoBack](#)

---

### Table of Contents

- **Register Function**

| Q0 | Store the returned address. If the interrupt instruction is a compressed one, the lowest bit of this register will be set. |
| Q1 | Contain a bitmask of all IRQs to be handled. This means one call to the interrupt handler needs to service more than one IRQ when more than one bit is set in Q1. |
| Q2 | Reserved. An option for ISR to store data. |
| Q3 | Reserved. An option for ISR to store data. |

**Note:**
- If more than one bits in Q1 are set, all the corresponding interrupts will call the same ISR. For such reason, users need to program ISR to check the interrupt number and execute corresponding program.
- After ULP-RISC-V is reset, all the interrupts are disabled.

All ISR entries are located at 0x10, and the reset entry is at 0x0.

---

### Section: Table 2.6-3. ULP-RISC-V Interrupt Registers

**2.6.3.3 Interrupt Handling**

When an interrupt occurs, ULP-RISC-V performs the following operations:
1. Saves the current PC to Q0.
2. Saves the interrupt being responded to in Q1.
3. Jumps to the interrupt entry point (0x10).

After ULP-RISC-V enters the interrupt entry point, please save the context and use Q2 and Q3 as temporary storage registers for backup. Before it exits the interrupt, restore the context. Then, exit the interrupt by executing the retiring instruction and jump to Q0. ULP does not support interrupt nesting and is not interrupted by any other interrupt before retiring irq is executed.

---

**2.6.3.4 Interrupt Instructions**

All these interrupt instructions are standard R-type instructions, with the same OpCode of custom0 (0001011). Figure 2.6-1 shows the format of standard R-type instructions. Note the fields funct3 (f3) and rs2 are ignored in these instructions.

**Figure Caption:**
Figure 2.6-1. Standard R-type Instruction Format

| func7 | rd    |
|--------|-------|
| 31     | 25, 24|
|        | 20, 19|
|        | 15, 14|
|        | 12, 11|
|        | 7,   6 |
|        | 0     |

**Instruction:**
getq rd,qs

This instruction copies the value of Qx into a general purpose register rd.

---

**Footer Information:**  
Espressif Systems  
324 ESP32-S3 TRM (Version 1.7)  

**Feedback Link:** [Submit Documentation Feedback](#)