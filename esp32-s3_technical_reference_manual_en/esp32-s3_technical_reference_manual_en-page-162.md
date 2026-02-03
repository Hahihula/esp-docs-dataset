**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.86 EE.VCMP.LT.S32

**Instruction Word Table:**
- 10 qa[2:1] 1110
- 0qa[0] qy[2] 1
- 0qy[1:0] qx[2:0]
- 00000100

**Assembler Syntax Heading:**
Assembler Syntax

**Syntax Example:**
EE.VCMP.LT.S32 qa, qx, qy

**Description Section:**
This instruction compares 32-bit vector data. It compares the numerical values of the four 32-bit data segments in registers qx and qy. If the former is smaller than the latter, it writes 0xFFFFFFF into the corresponding 32-bit data segment in register qa. Otherwise, it writes O to the segment.

**Operation Section:**
- qa[ 1: 0] = (qx[ 31: 0]<qy[ 31: 0]) ? 0xFFFFFFFF : 0
- qa[ 63: 32] = (qx[ 63: 32]<qy[ 63: 32]) ? 0xFFFFFFFF : 0
- ...
- qa[127:96] = (qx[127:96]<qy[127:96]) ? 0xFFFFFFFF : 0

**Footer Information:**
Espressif Systems  
Page Number: 162  
Document Title: ESP32-S3 TRM (Version 1.7)  
Link Texts:
- GoBack
- Submit Documentation Feedback