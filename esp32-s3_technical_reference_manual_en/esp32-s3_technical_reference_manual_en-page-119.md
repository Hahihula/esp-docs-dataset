**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.43 EE.MOVl.32.Q

**Subsection - Instruction Word Table:**
- 11 qu[2:1] 011
- 10 as[3:0] OI0O

**Subsection - Assembler Syntax:**
EE.MOVl.32.Q qu, as, 0..3

**Subsection - Description:**
This instruction assigns the value in register `as` to one data segment of 32 bits in register `qu` according to immediate number `se14`.

**Subsection - Operation (Code Block):**
```
if sel4 == 0:
    qu[ 31: 0] = as
if sel4 == 1:
    qu[63: 32] = as
if sel4 == 2:
    qu[95: 64] = as
if sel4 == 3:
    qu[127: 96] = as
```

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)