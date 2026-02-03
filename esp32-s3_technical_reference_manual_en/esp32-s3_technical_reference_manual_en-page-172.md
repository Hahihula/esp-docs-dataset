**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.96 EE.VLDBEC.16.XP

**Subsection - Instruction Word Table:**
- qu[2:1]: 101, 1101
- qu[0]: 100
- ad[3:0]: 
- as[3:0]: 
- 0100

**Subsection Title:**
Assembler Syntax

**Body Text - Description:**
EE.VLDBEC.16.XP qu, as, ad

This instruction forces the lower 11 bit of the access address in register `as` to 0, loads 16-bit data from memory, and broadcasts it to the eight 16-bit data segments in register `qu`. After the access is completed, the value in register `as` is incremented by the value in register `ad`.

**Subsection Title:**
Operation

**Body Text - Code Block:**
```
1   qu[127:0] = {8(load16({as[31:1], 1{0}}))}
2   as = as + ad[31:0]
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback