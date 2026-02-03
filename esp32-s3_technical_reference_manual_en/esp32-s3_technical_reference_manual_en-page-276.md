**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Link:**
GoBack

**Section Title:**
1.8.193 EE.VST.128.XP

**Subsection - Instruction Word Table:**
- 10
- qv[2:1] -> 1101
- qv[0]
- ad[1:1] -> 111
- as[3:0] -> 0100

**Subsection Title:**
Assembler Syntax

**Syntax Example:**
EE.VST.128.XP qv, as, ad

**Subsection - Description:**
This instruction forces the lower 4 bits of the access address in register as to zero and stores the 128 bits in register qv to memory. After the access is completed, the value in register as is incremented by the value in register ad.

**Subsection Title:**
Operation

**Code Example:**
```
1   qv[127:0] => store128({as[31:4], 4{0}})
2   as[31:0] = as[31:0] + ad[31:0]
```

**Footer Information:**
Espressif Systems
Page Number - 276
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback