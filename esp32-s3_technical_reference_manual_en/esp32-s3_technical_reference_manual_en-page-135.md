**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.59 EE.ST.ACCX.IP

**Instruction Word Table:**
- `0` | `imm8[7]` | `0000100` | `imm8[6:0]` | `as[3:0]` | `0100`

**Subtitle: Assembler Syntax**

**Body Text:**
EE.ST.ACCX.IP as, -512..508

**Description Section:**
This instruction forces the lower 3 bits of the access address in register as to 0, zero-extends special register ACCX to 64 bits, and stores the result to memory. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 3.

**Operation Section:**
1. `{24[0],ACCX[39:0]} = store64({as[31:3],3{0}})`
2. `as += imm8`

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback