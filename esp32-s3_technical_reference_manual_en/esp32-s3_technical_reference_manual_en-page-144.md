**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.68 EE.STF.64.XP

**Subsection - Instruction Word:**
- fv0[3:0] | 0111 | fv1[3:0] | ad[3:0] | as[3:0] | 0000

**Subsection - Assembler Syntax:**
EE.STF.64.XP fv1, fv0, as, ad

**Subsection - Description:**
This instruction forces the lower 3 bits of the access address in register `as` to zero and stores the 64-bit data concatenated from two floating-point registers `fv0` and `fv1` in order from low bit to high bit to memory. After the access is completed, the value in register `as` is incremented by the value in register `ad`.

**Subsection - Operation:**
```
{fv1, fv0} => store64({as[31:3], 3{0}})
as[31:0] = as[31:0] + ad[31:0]
``` 

**Footer Information:**
- Page number: 144
- Company name: Espressif Systems
- Document version and title: ESP32-S3 TRM (Version 1.7)
- Link text at the bottom right corner: Submit Documentation Feedback