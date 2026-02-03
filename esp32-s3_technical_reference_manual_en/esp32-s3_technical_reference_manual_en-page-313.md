**Chapter 2: ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

---

### Operands and Instructions Table:

| ALU_sel | Instruction    | Operation                          | Description                                    |
|---------|-----------------|------------------------------------|------------------------------------------------|
| 0       | STAGE_INC       | Stage_cnt = Stage_cnt + Imm        | Increment stage count register                 |
| 1       | STAGE_DEC       | Stage_cnt = Stage_cnt - Imm        | Decrement stage count register                 |
| 2       | STAGE_RST       | Stage_cnt = 0                      | Reset stage count register                     |

**Table Caption:**
- **Title:** Table 2.5-3. ALU Operations with Stage Count Register

**Note on Usage of Instructions in the Table:**
This instruction is mainly used with JUMPS instruction based on the stage count register to form a stage count for-loop.
For usage details, refer to pseudocode provided below.

---

### Pseudocode Example:

```plaintext
STAGE_RST // clear stage count register
STAGE_INC // stage count register++
{...}
// loop body, containing n instructions

JUMPS (step = n, cond = 0, threshold = m) // If the value of stage count register is less than m, then jump to STAGE_INC, otherwise jump out of the loop. By such way, a cumulative-for-loop with threshold m is implemented.
```

---

### Section: **2.5.2.2 - ST – Store Data in Memory**

**Figure Caption:** Figure 2.5-5 illustrates Instruction Type for "ST".

| Offset | Description |
|--------|-------------|
| Rdst   | Register R[0-3], address of the destination, expressed in 32-bit words |
| Rsrc   | Register R[0-3], 16-bit value to store |

**Table Caption:**
- **Title:** Automatic Storage Mode

**Table Description for Automatic Storage Mode:**

| Offset | Description |
|--------|-------------|
| upper  | Data label, 2-bit user defined unsigned value |
| wr_way | Write mode options (0: write the low half-word; 1: write the high half-word) |
| offset | 11-bit signed value, expressed in 32-bit words |
| wr_auto | Enable automatic storage mode |
| offset_set | Offset enable bit |

**Table Description for Automatic Storage Mode Options:** 

- **0:** Do not configure the offset for automatic storage mode.
- **1:** Configure the offset for automatic storage mode.

---

**Footer:**
- Page number 313
- Document version ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems

**Feedback Link:** Submit Documentation Feedback