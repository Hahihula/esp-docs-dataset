**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.19 EE.LD.ACCX.IP

**Instruction Word Table:**
| 0 | imm8[7] | 0011100 | imm8[6:0] | as[3:0] | 0100 |
|---|---------|---------|----------|--------|------|

**Subsection Title:**
Assembler Syntax

**Syntax Description:**
EE.LD.ACCX.IP as, -1024..1016

**Description Section:**
This instruction forces the lower 3 bits of the access address in register `as` to zero, loads 64-bit data from memory, and saves its lower 40 bits to the special register ACCX. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 3.

**Operation Section:**
1. `ACCX[39:0] = load64({as[31:3],3{0}})`
2. `as[31:0] = as[31:0] + {21{imm8[7]},imm8[7:0],3{0}}`

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version:**
ESP32-S3 TRM (Version 1.7)