**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.212 EE.VZIP.8

**Instruction Word:**
- 11 qs[2:1] 1100 qs[0] qsO[2:0] O01111010100

**Assembler Syntax:**
EE.VZIP.8 qsO, qs1

**Description:**
This instruction implements the zip algorithm on 8-bit vector data.

**Operation Table (Markdown format):**

| Operation | Value |
|-----------|-------|
| qsO[7:6] = 0; | |
| qsO[15:8] = qs1[7:0]; | |
| qsO[23:16] = qsS[15:8]; | |
| qsO[31:24] = qs1[15:8]; | |
| qsO[39:32] = qsO[23:16]; | |
| qsO[47:40] = qs1[23:16]; | |
| qsO[55:48] = qsS[31:24]; | |
| qsO[63:56] = qs1[31:24]; | |
| qsO[71:64] = qsS[39:32]; | |
| qsO[79:72] = qs1[39:32]; | |
| qsO[87:80] = qsS[47:40]; | |
| qsO[95:88] = qs1[47:40]; | |
| qsO[103:96] = qsS[55:48]; | |
| qsO[111:104] = qs1[55:48]; | |
| qsO[119:122] = qs1[63:56]; | |
| qsO[127:120] = qsS[71:64]; | |
| qsS[7:6] = 0; | |
| qsS[15:8] = qsS[71:64]; | |
| qsS[23:16] = qsO[79:72]; | |
| qsS[31:24] = qsO[79:72]; | |
| qsS[39:32] = qsO[87:80]; | |
| qsS[47:40] = qsO[87:80]; | |
| qsS[55:48] = qsO[95:88]; | |
| qsS[63:56] = qsO[95:88]; | |
| qsS[71:64] = qsO[103:96]; | |
| qsS[79:72] = qsO[103:96]; | |
| qsS[87:80] = qsO[111:104]; | |
| qsS[95:88] = qsO[111:104]; | |
| qsS[103:96] = qsO[119:122]; | |
| qsS[111:104] = qsO[119:122]; | |
| qsS[119:122] = qsO[127:120]; | |
| qsS[127:120] = qsO[127:120]; |

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback