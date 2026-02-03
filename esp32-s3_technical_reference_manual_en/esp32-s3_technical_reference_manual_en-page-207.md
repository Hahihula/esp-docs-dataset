**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.131 EE.VMUL.U8

**Subheader - Instruction Word:**
- 10, qz[2:1], 1110, qz[0], qy[2], 1, qy[1:0], qx[2:0], 10110100

**Subheader - Assembler Syntax:**
EE.VMUL.U8 qz, qx, qy

**Subheader - Description:**
This instruction performs an unsigned vector multiplication on 8-bit data. Registers qx and qy are the multiplier and the multiplicand respectively. The 16 bit-16 data results obtained from the calculation is logically right-shifted by the value in special register SAR. Then, the lower 8-bit data of the shift result is written into corresponding segment of register qz.

**Subheader - Operation:**
A table showing various operations with specific values for qx and qy:
- Example entries include:
  - `qz[7:0] = (qx[7:0] * qy[7:0]) >> SAR[5:0]`
  - `qz[15:8] = (qx[15:8] * qy[15:8]) >> SAR[5:0]`
  - And many more similar entries.

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)

**Navigation Links:**
- GoBack

**Document Feedback Link:** 
Submit Documentation Feedback