**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.73 EE.VADDS.S32

**Subsection - Instruction Word:**
- 10 qa[2:1] 1110 qa[0] qy[2] 0 qy[1:0] qx[2:0] 01110100

**Subsection - Assembler Syntax:**
EE.VADDS.S32 qa, qx, qy

**Subsection - Description:**
This instruction performs a vector addition on 32-bit data in the two registers qx and qy. Then, the 4 results obtained from the calculation are saturated, and the saturated results are written to register qa.

**Subsection - Operation (with code block):**
```
qa[ 31: 0 ] = min(max(qx[ 31: 0 ] + qy[ 31: 0 ], -2^31), 2^31-1)
qa[ 63: 32 ] = min(max(qx[ 63: 32 ] + qy[ 63: 32 ], -2^31), 2^31-1)
...
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)

**Link Texts at the Bottom of Page:**
Submit Documentation Feedback