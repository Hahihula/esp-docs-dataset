**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.72 EE.VADDS.S16.ST.INCP

**Instruction Word Table:**
- Instruction Word:
  - 1100100 | qy[0] | qv[2:0] | 1 | qa[2:0] | qx[1:0] | qy[2:1] | 0000 | as[3:0] | 111 | qx[2]

**Subsection Title:**
Assembler Syntax

**Subsection Content:**
EE.VADDS.S16.ST.INCP qv, as, qx, qy

**Subsection Title:**
Description

**Subsection Content:**
This instruction performs a vector addition on 16-bit data in the two registers qx and qy. Then, the 8 results obtained from the calculation are saturated, and the saturated results are written to register qa.

During the operation, the instruction forces the lower 4 bits of the access address in register as to 0 and stores the value in register qv to memory. After the access, the value in register as is incremented by 16.

**Subsection Title:**
Operation

**Subsection Content (List):**
```
qa[ 15: 0 ] = min(max(qx[ 15: 0 ] + qy[ 15: 0 ], -2^{15}-1)
qa[ 31: 16 ] = min(max(qx[ 31: 16 ] + qx[ 31: 16 ], -2^{15}-1)
...
qv[127:0] => store128({as[31:4],4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
Espressif Systems

**Document Version and Feedback Link:**
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback