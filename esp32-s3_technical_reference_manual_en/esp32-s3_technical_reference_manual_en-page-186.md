**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.110 EE.VMAX.S8

**Instruction Word Table:**
- 10 qa[2:1] 1110
- 10 qa[0] qy[2]
- 1 qy[1:0]
- 1 qy[2:0]
- 01000100

**Subheader - Assembler Syntax:**
EE.VMAX.S8 qa, qx, qy

**Description Section:**
This instruction compares numerical values of the 16 8-bit vector data segments in registers qx and qy. The data segment with the larger value is written into the corresponding 8-bit data segment in register qa.

**Operation Table (Markdown format):**

```
qa[7:0] = (qx[7:0] > qy[7:0]) ? qx[7:0] : qy[7:0]
qa[15:8] = (qx[15:8] > qy[15:8]) ? qx[15:8] : qy[15:8]
...
qa[127:120] = (qx[127:120] > qy[127:120]) ? qx[127:120] : qy[127:120]
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback