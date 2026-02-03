**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.94 EE.VLDBC.16

**Subsection - Instruction Word:**
- 11 qu[2:1] 1101 qu[0] 1110011 as[3:0] 0100

**Subsection - Assembler Syntax:**
EE.VLDBC.16 qu, as

**Subsection - Description:**
This instruction forces the lower 11 bit of the access address in register `as` to 0, loads 16-bit data from memory, and broadcasts it to the eight 16-bit data segments in register `qu`.

**Subsection - Operation:**
```
qu[127:0] = {8(load16({as[31:1],1{0}}))}
``` 

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback