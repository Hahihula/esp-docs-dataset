**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.80 EE.VCMP.EQ.S32

**Instruction Word Table:**
- 10 qa[2:1] 1110 qa[0] 0 qy[2] 0 qx[1:0] 0 xq[2:0] 10100100

**Subsection Title:**
Assembler Syntax

**Syntax Example:**
EE.VCMP.EQ.S32 qx, qy

**Description Section:**
This instruction compares 32-bit vector data. It compares the numerical values of the four 32-bit data segments in registers qx and qy. If the values are equal, it writes 0xFFFFFFFF into the corresponding 32-bit data segment in register qa. Otherwise, it writes 0 to the segment.

**Operation Section:**
- `qa[ 31: 0 ] = (qx[ 31: 0 ] == qy[ 31: 0 ]) ? 0xFFFFFFFF : 0`
- `qa[63: 32] = (qx[63: 32] == qy[63: 32]) ? 0xFFFFFFFF : 0`
- ...
- `qa[127:96] = (qx[127:96] == qy[127:96]) ? 0xFFFFFFFF : 0`

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback