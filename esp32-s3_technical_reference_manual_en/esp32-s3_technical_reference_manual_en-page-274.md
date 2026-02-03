**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.191 EE.VSR.32

**Instruction Word Breakdown Table:**
- 11 qs[2:1]
- 1101 qs[0]
- 01111111 qa[2:0]
- 0100

**Subsection Title:**
Assembler Syntax

**Syntax Example:**
EE.VSR.32 qa, qs

**Description Section:**
This instruction performs an arithmetic right shift on the four 32-bit data segments in register qs respectively.

The shift amount is the value in the 6-bit special register SAR. During the shift process, the higher bits are padded with signed bit. The lower 32 bits of the shift result are stored in the corresponding data segment in register qa.

**Operation Section:**
1. qa[ 31: 0 ] = (qs[ 31: 0 ] >> SAR[5:0])
2. qa[63: 32] = (qs[63: 32] >> SAR[5:0])
3. qa[95: 64] = (qs[95: 64] >> SAR[5:0])
4. qa[127: 96] = (qs[127: 96] >> SAR[5:0])

**Footer Information:**
Espressif Systems
Page Number: 274 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback