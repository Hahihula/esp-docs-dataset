**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.97 EE.VLDBC.32

**Subsection - Instruction Word:**
- 11 qu[2:1] 1101 qu[0] 111011 as[3:0] O100

**Subsection - Assembler Syntax:**
EE.VLDBC.32 qu, as

**Subsection - Description:**
This instruction forces the lower 2 bits of the access address in register `as` to zero and loads 32-bit data from memory and broadcasts it to the four 32-bit data segments in register `qu`.

**Subsection - Operation:**
```
qu[127:0] = {4|load32({as[31:2],2{0}})}
``` 

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback