**Chapter Title:**
Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)

**Figure Caption and Description for Figure 2.5-6:**
- **Title:** Instruction Type - Offset in Automatic Storage Mode (ST-OFFSET)
- **Description:** Operand Description
- **Text under the figure caption:** "offset Initial address offset, 11-bit signed value, expressed in 32-bit words"

**Figure Caption and Description for Figure 2.5-7:**
- **Title:** Instruction Type - Data Storage in Automatic Storage Mode (ST-AUTO-DATA)
- **Description:** Operand Description
- **Text under the figure caption:** "Rdst Register R[0-3], address of the destination, expressed in 32-bit words

**Table Content for Figure 2.5-7:**
```
| 31 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9  |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|    |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
| 06 |   1 |   2 |   3 |   4 |   5 |   6 |   7 |   8 |   9 |  A  | B  | C  | D  | E  | F  | G  | H  | I  |
```

**Description for ST-AUTO-DATA Instruction:**
- **Text:** "This mode is used to access continuous addresses. Before using this mode for the first time, please configure the initial address using ST-OFFSET instruction. Executing the instruction ST-AUTO-DATA will store the 16-bit data in Rsra into the memory address Rdst + Offset, see Table 2.5-4. Write_cnt here indicates the times of the instruction ST-AUTO-DATA executed."

**Footer:**
- "Espressif Systems"
- Page number and document version information:
  - **Page Number:** 314
  - **Document Version Information:** ESP32-S3 TRM (Version 1.7)
  - Link for submitting documentation feedback.

**Navigation Links:**
- GoBack

(Note: The text "label" in the table is part of a binary representation and not an actual label or code block.)