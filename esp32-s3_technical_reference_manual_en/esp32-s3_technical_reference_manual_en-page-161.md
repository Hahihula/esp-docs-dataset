**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.85 EE.VCMLT.S16

**Instruction Word Table:**
- 10 qa[2:1] 1110 qa[0] qy[2] 0 qy[1:0] qx[2:0] 1110100

**Assembler Syntax Section:**
- EE.VCMLT.S16 qa, qx, qy

**Description Section:**
This instruction compares 16-bit vector data. It compares the numerical values of the eight 16-bit data segments in registers qx and qy. If the former is smaller than the latter, it writes 0xFFFF into the corresponding 16-bit data segment in register qa. Otherwise, it writes 0 to the segment.

**Operation Section:**
- qa[ 5: 0 ] = (qx[ 15: 16 ]<qy[ 15: 16 ]) ? 0x{FFFF} : 0
- qa[31:16] = (qx[31:16]<qy[31:16]) ? 0x{FFFF} : 0

**Additional Operations Listed in the Image but not described with syntax or explanation:** 
- ...
- qa[127:112] = (qx[127:112]<qy[127:112]) ? 0x{FFFF} : 0

**Footer Information:**
Espressif Systems
Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)