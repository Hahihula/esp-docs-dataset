**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Section Header:**
GoBack

---

### Figure Caption:
- **Figure 2.6-2. Interrupt Instruction - getq rd, qs**

#### Table:
| 31 | 25 | 24 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0000000 | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | 0 |
|        |     |    |    |    |    |    |    |    |    |    |    |    | 0001011 |

#### Text:
- **Operand Description** - See Figure 2.6-2
  - `rd` Target general purpose register, holds the value of interrupt register specified by qs.
  - `qs` Address of interrupt register Qx.
  - `f7` Interrupt instruction number.

- **Instruction: setq qd,rs**
  This instruction copies the value of general purpose register rs to Qx.

---

### Figure Caption:
- **Figure 2.6-3. Interrupt Instruction - setq qd,rs**

#### Table:
| 31 | 25 | 24 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0000001 | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | 0 |
|        |     |    |    |    |    |    |    |    |    |    |    |    | 0001011 |

#### Text:
- **Operand Description** - See Figure 2.6-3
  - `qd` Target interrupt register.
  - `rs` Source general purpose register, stores the value to be written to interrupt register.
  - `f7` Interrupt instruction number.

- **Instruction: retireq**
  This instruction copies the value of QO to CPU PC, and enables interrupt again.

---

### Figure Caption:
- **Figure 2.6-4. Interrupt Instruction - retireq**

#### Table:
| 31 | 25 | 24 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0000010 | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | 0 |
|        |     |    |    |    |    |    |    |    |    |    |    |    | 0001011 |

#### Text:
- **Operand Description** - See Figure 2.6-4
  - `f7` Interrupt instruction number.

- **Instruction: maskirq rd,rs**
  This instruction copies the value of the register IRQ Mask to the register rd, and copies the value of register rs to IRQ Mask.

---

**Footer Information:**
Espressif Systems  
325  
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback