**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.76 EE.VADDS.S8

**Subsection - Instruction Word:**
```
10   qa[2:1] 1110   qa[0]   qy[2]    0   qy[1:0]   qx[2:0]   10000100
```

**Subsection - Assembler Syntax:**
EE.VADDS.S8 qa, qx, qy

**Subsection - Description:**
This instruction performs a vector addition on 8-bit data in the two registers qx and qy. Then, the 16 results obtained from the calculation are saturated, and the saturated results are written to register qa.

**Subsection - Operation (with code block):**
```
qa[7:0] = min(max(qx[7:0] + qy[7:0], -2^7), 2^7-1)
qa[15:8] = min(max(qx[15:8] + qy[15:8], -2^7), 2^7-1)
...
qa[127:120] = min(max(qx[127:120] + qy[127:120], -2^7), 2^7-1)
```

**Footer Information:**
Espressif Systems
Page number: 152
Document version and title: ESP32-S3 TRM (Version 1.7)

**Link Texts:**
GoBack, Submit Documentation Feedback