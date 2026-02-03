**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
GoBack

**Subheading:**
1.8.102 EE.VLDBEC.8.XP

**Instruction Word Table:**
- qu[2:1] = 1101
- qu[0] = 101
- ad[3:0] = as[3:0]
- as[3:0] = 0100

**Subheading:**
Assembler Syntax

**Syntax Example:**
EE.VLDBEC.8.XP qu, as, ad

**Subheading:**
Description

**Body Text:**
This instruction loads 8-bit data from memory at the address given by the access register `as` and broadcasts it to the 16 8-bit data segments in register `qu`. After the access is completed, the value in register `as` is incremented by the value in register `ad`.

**Subheading:**
Operation

**Body Text with Code Example:**
```
qu[127:0] = {16[load8(as[31:0])]}
as = as + ad[31:0]
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback