**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.34 EE.LDQA.U16.128.XP

**Subheading - Instruction Word:**
01110100100 ad[3:0] as[3:0] 0100

**Subheading - Assembler Syntax:**
EE.LDQA.U16.128.XP as, ad

**Subheading - Description:**
This instruction forces the lower 4 bits of the access address in register as to 0, loads 16-byte data from memory, divides it into 8 segments of 16 bits, zero-extends each segment to 40 bits, and then stores the results to the 160-bit special registers QACC_L and QACC_H respectively. After the access is completed, the value in register as is incremented by the value in register ad.

**Subheading - Operation:**
```
dataIn[127:0] = load128({as[31:4], 4{0}})
QACC_L[39: 0] = {24{0}, dataIn[ 15: 0]}
...
QACC_H[159:120] = {24{0}, dataIn[127:112]}
as[31:0] = as[31:0] + ad[31:0]
```

**Footer Information:**
Espressif Systems
Page number 110

**Document Version and Feedback Link:**
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback