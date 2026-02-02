**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**GoBack Link:** [GoBack](#)

---

### Table of Contents

- **Operand Description - see Figure 1.4-2**

| ALU_sel | Instruction | Operation | Description |
|---------|-------------|-----------|-------------|
| 0       | ADD         | Rdst = Rsrc1 + Rsrc2 | Add to register |
| 1       | SUB         | Rdst = Rsrc1 - Rsrc2 | Subtract from register |
| 2       | AND         | Rdst = Rsrc1 & Rsrc2 | Bitwise logical AND of two operands |
| 3       | OR          | Rdst = Rsrc1 | bitwise logical OR of two operands |
| 4       | MOVE        | Rdst = Rsrc1 | Move to register |
| 5       | LSH         | Rdst = Rsrc1 << Rsrc2 | Bit shifting Left |
| 6       | RSH         | Rdst = Rsrc1 >> Rsrc2 | Bit shifting Right |

**Table Caption:**
Table 1.4-1 ALU Operations Among Registers

---

### Note:
- ADD/SUB operations can be used to set/clear the overflow flag in ALU.
- All ALU operations can be used to set/clear the zero flag in ALU.

---

#### Subsection Title
**1.4.1.2 Operations with Immediate Value**

**Figure Caption:**
Figure 1.4-3 Instruction Type — ALU for Operations with Immediate Value

**Table Description (from Figure):**
When bits [27:25] of the instruction in Figure 1.4-3 are set to 3'b1, ALU performs operations using register R[0-3] and the immediate value stored in [19:4]. The types of operations depend on the setting of the instruction's bits presented in Table 1.4-2.

**Table for Immediate Value Operations (from Figure):**
| ALU_sel | Imm |
|---------|-----|
| 3d7     | Rsrc1, Rdst |

---

### Footer
- **Page Number:** Page 32 of ESP32 TRM (Version 5.6)
- **Company Name:** Espressif Systems

**Link:**
[Submit Documentation Feedback](#)