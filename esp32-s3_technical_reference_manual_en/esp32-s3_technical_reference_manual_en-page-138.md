**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.62 EE.ST.QACC_L.H.32.IP

**Subsection - Instruction Word Table:**
- Columns are labeled as `imm4[7]`, `011010`, `imm4[6:0]`, `as[3:0]`, and `0100`.

**Subsection Title:**
Assembler Syntax

**Body Text (Description):**
This instruction forces the lower 2 bits of the access address in register as to zero and stores the upper 32 bits in special register QACC_L to memory. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 2.

**Subsection Title:**
Operation

**Body Text (Code):**
1. `QACC_L[159:128]` => `store32({as[31:2],2{0}})`
2. `as[31:0] = as[31:0] + {23{imm4[7]},imm4[7:0],2{0}}`

**Footer Information:**
- Page number 138
- Document title ESP32-S3 TRM (Version 1.7)
- Company name Espressif Systems

**Link Texts:**
- GoBack
- Submit Documentation Feedback