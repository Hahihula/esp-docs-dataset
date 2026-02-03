**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.163 EE.VMULAS.U16.QACC

**Instruction Word Table:**
- Instruction Word: `0000100` | `qy[2]` | `1` | `qy[1:0]` | `qx[2:0]` | `10000100`

**Assembler Syntax Section Title:**
Assembler Syntax

**Assembler Syntax Content:**
EE.VMULAS.U16.QACC qx, qy

**Description Section Title:**
Description

**Description Text:**
This instruction divides registers qx and qy into 8 data segments by 16 bits. Then, the unsigned multiplication result of the 8 sets of segments is added to the corresponding 40-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 40-bit unsigned number and then stored to the corresponding 40-bit data segment in QACC_H and QACC_L.

**Operation Section Title:**
Operation

**Operation Text with Code Blocks (Markdown format):**
1. `QACC_L[39:0] = min(QACC_L[39:0] + qx[15:0] * qy[15:0], 2^{40}-1)`
2. `QACC_L[79:40] = min(QACC_L[79:40] + qx[31:16] * qy[31:16], 2^{40}-1)`
...
5. `QACC_H[79:40] = min(QACC_H[79:40] + qx[95:80] * qy[95:80], 2^{40}-1)`
...
8. `QACC_H[159:120] = min(QACC_H[159:120] + qx[127:112] * qy[127:112], 2^{40}-1)`

**Footer Information:**
Espressif Systems
Page Number: 245

**Document Version and Link Section Title:**
ESP32-S3 TRM (Version 1.7)

**Link Texts in Footer:**
Submit Documentation Feedback