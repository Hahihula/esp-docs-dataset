**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.89 EE.VLD.128.XP

**Subsection - Instruction Word Table:**
- `qu[2:1]`: 1101
- `qu[0]`: 010
- `ad[3:0]`: 
- `as[3:0]`: 
- `0100`

**Subsection Title:**
Assembler Syntax

**Syntax Description:**
EE.VLD.128.XP qu, as, ad

**Description Section:**
This instruction forces the lower 4 bits of the access address in register as to 0 and loads 16-byte data from memory to register ad. After the access is completed, the value in register as is incremented by the value in register ad.

**Operation Section (with code example):**
```
qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + ad[31:0]
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback