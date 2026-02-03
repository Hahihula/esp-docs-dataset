**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.198 EE.VSUBS.S16

**Subsection - Instruction Word:**
- 10 qa[2:1] 1110 qa[0] qy[2] 1 qy[1:0] qx[2:0] 11010100

**Subsection - Assembler Syntax:**
EE.VSUBS.S16 qa, qx, qy

**Subsection - Description:**
This instruction performs a vector subtraction on 16-bit data. Registers qx and qy are the subtrahend and the minuend respectively. Then, the 8 results obtained from the calculation are saturated and then written into register qa.

**Subsection - Operation (with code block):**
```
qa[ 15: 0 ] = min(max(qx[ 15: 0 ] - qy[ 15: 0 ], -2^15), 2^15-1)
qa[ 31: 16 ] = min(max(qx[ 31: 16 ] - qy[ 31: 16 ], -2^15), 2^15-1)
...
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)

**Link Texts:**
GoBack, Submit Documentation Feedback