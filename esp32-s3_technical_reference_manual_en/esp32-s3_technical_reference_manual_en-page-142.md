**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.66 EE.STF.128.XP

**Subsection - Instruction Word Table:**
- `Instruction Word`
  - `10011` 
    - `fv3[3:1]`
    - `fv0[0:3]`
    - `fv3[0]`
    - `fv2[3:1]`
    - `fv1[3:0]`
    - `ad[3:0]`
    - `as[3:0]`
    - `111`
    - `fv2[0]`

**Subsection - Assembler Syntax:**
- `EE.STF.128.XP fv3, fv2, fv1, fv0, as, ad`

**Subsection - Description:**
This instruction forces the lower 4 bits of the access address in register `as` to zero and stores the 16-byte data concatenated from four floating-point registers `fu0`, `fu1`, `fu2`, and `fu3` in order from low bit to high bit to memory. After the access is completed, the value in register `as` is incremented by the value in register `ad`.

**Subsection - Operation:**
```
{fv3, fv2, fv1, fv0} => store128({as[31:4], 4{0}})
as[31:0] = as[31:0] + ad[31:0]
``` 

**Footer Information:**
- "Espressif Systems"
- Page number: `142`
- Document version and title: "ESP32-S3 TRM (Version 1.7)"
- Link text at the bottom right corner:
  - "Submit Documentation Feedback"