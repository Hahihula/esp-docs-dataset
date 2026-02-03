**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.36 EE.LDQA.U8.128.XP

**Subsection - Instruction Word:**
011100000100 as[3:0] as[3:0] 0100

**Subsection - Assembler Syntax:**
EE.LDQA.U8.128.XP as, ad

**Subsection - Description:**
This instruction forces the lower 4 bits of the access address in register as to 0, loads 16-byte data from memory, divides it into 16 segments of 8 bits, zero-extends each segment to 20 bits, and then stores the results to the 160-bit special registers QACC_L and QACC_H respectively. After the access is completed, the value in register as is incremented by the value in register ad.

**Subsection - Operation:**
```
dataIn[127:0] = load128({as[31:4], 4{0}})
QACC_L[19: 0] = {12{0}, dataIn[ 7: 0]}
...
QACC_L[159:140] = {12{0}, dataIn[ 63: 56]}
QACC_H[ 19: 0] = {12{0}, dataIn[ 71: 64]}
QACC_H[159:140] = {12{0}, dataIn[127:120]}
as[31:0] = as[31:0] + ad[31:0]
```

**Footer Information:**
Espressif Systems
Page 112 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback