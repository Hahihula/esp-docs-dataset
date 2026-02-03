**Title: Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

**Subtitle: Operations with Immediate Value**

---

### Figure Caption:
- **Figure 2.5-3. Instruction Type — ALU for Operations with Immediate Value**
  
#### Body Text:
When bits [27:26] of the instruction in Figure `2.5-3` are set to 1, ALU performs operations using register R[0-3] and the immediate value stored in instruction bits [19:4]. The types of operations depend on the setting of the instruction bits ALU_sel[24:21] presented in Table `2.5-2`.

#### Table:
| Operand | Description - see Figure 2.5-3 |
|---------|----------------------------------|
| Rdst    | Register R[0-3], destination     |
| Rs1c    | Register R[0-3], source         |
| Imm     | 16-bit signed immediate value   |

ALU operation selection, see Table `2.5-2`

#### Table:
| ALU_sel | Instruction Type | Operation | Description |
|---------|------------------|-----------|------------|
| 0       | ADD              | Rdst = Rs1c + Imm | Add to register |
| 1       | SUB              | Rdst = Rs1c - Imm | Subtract from register |
| 2       | AND              | Rdst = Rs1c & Imm | Bitwise logical AND of two operands |
| 3       | OR               | Rdst = Rs1c | Imm | Bitwise logical OR of two operands |
| 4       | MOVE             | Rdst = Imm    |           | Move to register |
| 5       | LSH              | Rdst = Rs1c << Imm | Bit shifting left |
| 6       | RSH              | Rdst = Rs1c >> Imm | Bit shifting right |

---

### Figure Caption:
- **Figure 2.5-4. Instruction Type — ALU for Operations with Stage Count Register**

#### Body Text:
ALU is also able to increment or decrement by a given value, or reset the 8-bit register Stage_cnt. To do so, bits [27:26] of instruction in Figure `2.5-4` should be set to 2. The type of operation depends on the setting of the instruction bits ALU_sel[24:21] presented in Table `2.5-4`. The Stage_cnt is a separate register and is not a part of the instruction in Figure `2.5-4`.

---

**Note:**  
- ADD or SUB operations can be used to set or clear the overflow flag in ALU.
- All ALU operations can be used to set or clear the zero flag in ALU.

---

### Subtitle: Operations with Stage Count Register

#### Body Text:
ALU is also able to increment or decrement by a given value, or reset the 8-bit register Stage_cnt. To do so, bits [27:26] of instruction in Figure `2.5-4` should be set to 2. The type of operation depends on the setting of the instruction bits ALU_sel[24:21] presented in Table `2.5-4`. The Stage_cnt is a separate register and is not a part of the instruction in Figure `2.5-4`.

---

**Footer:**  
Espressif Systems  
312 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback