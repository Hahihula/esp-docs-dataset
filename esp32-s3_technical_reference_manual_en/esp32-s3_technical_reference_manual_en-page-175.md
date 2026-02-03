**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.99 EE.VLDBEC.32.XP

**Instruction Word Table:**
- `qu[2:1]`: 10
- `qu[0]`: 1101
- `ad[3:0]`: 0001
- `as[3:0]`: ad[3:0]
- `0100`

**Subsection Title:**
Assembler Syntax

**Syntax:**
EE.VLDBEC.32.XP qu, as, ad

**Description Section:**
This instruction forces the lower 2 bits of the access address in register as to 0, loads 32-bit data from memory and broadcasts it to the four 32-bit data segments in register qu. After the access is completed, the value in register as is incremented by the value in register ad.

**Operation Section:**
1. `qu[127:0] = {4{load32({as[31:2],2{0})}}}`
2. `as = as + ad[31:0]`

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback