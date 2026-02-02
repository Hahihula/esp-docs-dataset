**Title: Chapter 1 ULP Coprocessor (ULP)**

---

### Section Title:
1.4.4 JUMP – Jump to an Absolute Address

#### Figure Caption:
Figure 1.4-7. Instruction Type — JUMP

| Operands | Description |
|----------|-------------|
| Rdst     | Register R[0-3], address to jump to |
| ImmAddr | 11-bit address, expressed in 32-bit words |

**Type:**
- Jump type:
  - O – make an unconditional jump
  - I – jump only if the last ALU operation has set the zero flag
  - Z – jump only if the last ALU operation has set the overflow flag

#### Description:
The instruction prompts a jump to the specified address. The jump can be either unconditional or based on the ALU flag.

**Note:**
All jump addresses are expressed in 32-bit words.

---

### Section Title:
1.4.5 JUMPR – Jump to a Relative Offset (Conditional upon RO)

#### Figure Caption:
Figure 1.4-8. Instruction Type — JUMPR

| Operands | Description |
|----------|-------------|
| Step     | Relative shift from current position, expressed in 32-bit words: if Step[7] = 0 then PC = PC + Step[6:0] if Step[7] = 1 then PC = PC - Step[6:0] |
| Threshold| Threshold value for condition (see Cond below) to jump |
| Cond     | Condition to jump: O – jump if RO < Threshold I – jump if RO >= Threshold |

#### Description:
The instruction prompts a jump to a relative address, if the above-mentioned condition is true. The condition itself is the result of comparing the RO register value and the Threshold value.

**Note:**
All jump addresses are expressed in 32-bit words.

---

**Footer Information:**  
Espressif Systems  
Page number: 35  
Document version: ESP32 TRM (Version 5.6)  

[Submit Documentation Feedback](#)