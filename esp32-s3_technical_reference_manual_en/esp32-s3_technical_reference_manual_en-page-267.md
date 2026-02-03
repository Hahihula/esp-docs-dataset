**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.185 EE.VRELU.S8

**Instruction Word Table:**
- qs[2:1] | qs[0] | 101 | ax[3:0] | ay[3:0]
- 11   | 1101 | 0100

**Subsection Title:**
Assembler Syntax

**Syntax Example:**
EE.VRELU.S8 qs, ax, ay

**Description Section:**
This instruction divides register qs into 16 data segments by 8 bits. If the value of the segment is not greater than 0, it will be multiplied by the value of the lower 8 bits in register ax and right-shifted by the value of the lower 5 bits in register ay, and then the result obtained will overwrite the value of the segment. Otherwise, the value of the segment will remain unchanged.

**Operation Section:**
- qs[7:0] = (qs[7:0] <= 0) ? (qs[7:0] * ax[7:0]) >> ay[4:0] : qs[7:0]
- qs[15:8] = (qs[15:8] <= 0) ? (qs[15:8] * ax[7:0]) >> ay[4:0] : qs[15:8]
- ... 
- qs[127:120] = (qs[127:120] <= 0) ? (qs[127:120] * ax[7:0]) >> ay[4:0] : qs[127:120]

**Footer Information:**
Espressif Systems
Page Number: 267
Document Title: ESP32-S3 TRM (Version 1.7)
Link Texts:
- Submit Documentation Feedback