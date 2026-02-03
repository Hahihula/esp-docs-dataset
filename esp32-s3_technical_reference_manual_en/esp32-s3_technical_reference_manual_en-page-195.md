**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.119 EE.VMIN.S8

**Instruction Word Syntax Table:**
- `10 qa[2:1]`
- `1110 qa[0]`
- `qy[2]`
- `1 qy[1:0]`
- `qx[2:0]`
- `01110100`

**Subheading - Assembler Syntax:**
EE.VMIN.S8 qa, qx, qy

**Subheading - Description:**
This instruction compares numerical values of the 16 8-bit vector data segments in registers qx and qy. The data segment with the smaller value is written into the corresponding 8-bit data segment in register qa.

**Subheading - Operation (with code example):**
```
1    qa[7:0] = (qx[7:0] <= qy[7:0]) ? qx[7:0] : qy[7:0]
2    qa[15:8] = (qx[15:8] <= qy[15:8]) ? qx[15:8] : qy[15:8]
3
4    qa[127:120] = (qx[127:120] <= qy[127:120]) ? qx[127:120] : qy[127:120]
``` 

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback