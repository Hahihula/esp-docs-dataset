**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.201 EE.VSUBS.S32

**Subsection - Instruction Word:**
- `10`
- `qa[2:1]` -> `1110`
- `qa[0]` -> `1`
- `qy[2]` -> `1`
- `qy[1:0]` -> `00`
- `qx[2:0]` -> `1100`

**Subsection - Assembler Syntax:**
EE.VSUBS.S32 qa, qx, qy

**Subsection - Description:**
This instruction performs a vector subtraction on 32-bit data. Registers qx and qy are the subtrahend and the minuend respectively. Then, the 4 results obtained from the calculation are saturated and then written into register qa.

**Subsection - Operation (with code block):**

```
1    qa[ 31:0 ] = min(max(qx[ 31:0 ] - qy[ 31:0 ], -2^31), 2^31-1)
2    qa[ 63:32 ] = min(max(qx[ 63:32 ] - qy[ 63:32 ], -2^31), 2^31-1)
...
```

**Footer Information:**
Espressif Systems
Page number: `284`
Document version and title: ESP32-S3 TRM (Version 1.7)

**Link Texts:**
GoBack, Submit Documentation Feedback