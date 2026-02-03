**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.206 EE.VSUBS.S8.ST.INCP

**Subsection - Instruction Word:**
- 11101000 qy[0] qv[2:0] 1 qa[2:0] qx[1:0] qy[2:1] 0011 as[3:0] 111 qx[2]

**Subsection - Assembler Syntax:**
EE.VSUBS.S8.ST.INCP qv, as, qa, qx, qy

**Subsection - Description:**
This instruction performs a vector subtraction on 8-bit data. Registers qx and qy are the subtrahend and the minuend respectively. Then, the 16 results obtained from the calculation are saturated and then written into register qa.

During the operation, the instruction forces the lower 4 bits of the access address in register as to 0 and stores the value in register qv to memory. After the access, the value in register as is incremented by 16.

**Subsection - Operation:**
```
qa[7:0] = min(max(qx[7:0] - qy[7:0], -2^7), 2^7-1)
qa[15:8] = min(max(qx[15:8] - qy[15:8], -2^7), 2^7-1)
...
qv[127:0] => store128({as[31:4],4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback

**Document Version and Title:** ESP32-S3 TRM (Version 1.7)