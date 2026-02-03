**Chapter 2: ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

---

### Operands and Description:
- **RdSt**: Register R[0-3], address of the destination, expressed in 32-bit words.
- **RsRC**: Register R[0-3], 16-bit value to store
- **label**: Data label, 2-bit user defined unsigned value

**upper**
- `0`: Write the low half-word; `1`: write the high half-word

**wr_way**
- `0`: Write the full-word; `1`: with the label; `3`: without the label

**offset**
- 11-bit signed value, expressed in 32-bit words

---

### Description:
Manual storage mode is mainly used for storing data into discontinuous addresses. Each instruction needs a storage address and offset.

The detailed storage methods are shown in Table 2.5-5:

| wr_way | upper | Data       | Operation                                    |
|--------|-------|-----------|----------------------------------------------|
| `0`    | `*`   | Mem [RdSt + Offset][31:0] = {PC[10:0],3'b0, Label[1:0],RsRC[15:0]} | Write full-word, including the pointer and the data |
|        |       |           | Store the data with label in the low half-word |
| `1`    | `1`   | Mem [RdSt + Offset][31:16] = {Label[1:0],RsRC[13:0]}  | Store the data with label in the high half-word     |
| `3`    | `0`   | Mem [RdSt + Offset][15:0] = RsRC[15:0]                | Store the data without label in the low half-word  |
| `3`    | `1`   | Mem [RdSt + Offset][31:16] = RsRC[15:0]               | Store the data without label in the high half-word |

---

**Table 2.5-5**: Data Storage - Manual Storage Mode

---

### Section Title:
**2.5.2.3 LD – Load Data from Memory**

---

### Figure Caption and Description:

#### **Figure 2.5-10: Instruction Type - LD**
- **Operand Description:** see Figure 2.5-10
  - **RdSt**: Register R[0-3], destination
  - **RsRC**: Register R[0-3], address of destination memory, expressed in 32-bit words
  - **Offset**: 11-bit signed value, expressed in 32-bit words

**rd_upper**
- Choose which half-word to read:
  - `1`: read the high half-word
  - `0`: read the low half-word

#### Description:

This instruction loads the low or high 16-bit half-word, depending on rd_upper, from memory with address RsRC + offset into the destination register RdSt.

RdSt[15:0] = Mem[RsRC + Offset]

---

**Footer Information:**  
Espressif Systems  
316  
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback