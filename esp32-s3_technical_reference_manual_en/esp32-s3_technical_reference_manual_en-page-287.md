**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.204 EE.VSUBS.S8

**Subsection - Instruction Word Table:**
- 10 qa[2:1] 1110
- 1110 qa[0]
- 1110 qa[2] 1
- 1110100 qx[1:0] qx[2:0]

**Subsection - Assembler Syntax:**
EE.VSUBS.S8 qa, qx, qy

**Subsection - Description:**
This instruction performs a vector subtraction on 8-bit data. Registers qx and qy are the subtrahend and the minuend respectively. Then, the 16 results obtained from the calculation are saturated and then written into register qa.

**Subsection - Operation Table (with code examples):**
- `qa[7:0] = min(max(qx[7:0] - qy[7:0], -2^7), 2^7) - 1`
- `qa[15:8] = min(max(qx[15:8] - qy[15:8], -2^7), 2^7) - 1`

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback