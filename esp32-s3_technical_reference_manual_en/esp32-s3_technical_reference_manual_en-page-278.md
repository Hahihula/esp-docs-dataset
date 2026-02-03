**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.195 EE.VST.H.64.XP

**Subsection - Instruction Word:**
- 11
- qv[2:1] 1101
- qv[0] 000
- ad[3:0] as[3:0]
- 0100

**Subsection - Assembler Syntax:**
EE.VST.H.64.XP qv, as, ad

**Subsection - Description:**
This instruction forces the lower 3 bits of the access address in register as to 0 and stores the upper 64 bits in register qv to memory. After the access is completed, the value in register as is incremented by the value in register ad.

**Subsection - Operation (with code block):**
```
1   qv[127: 64 ] = stored64({as[31:3],3{0}})
2   as = as + ad[31:0]
```

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)