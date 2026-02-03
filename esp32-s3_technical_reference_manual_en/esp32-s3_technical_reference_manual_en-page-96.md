**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.20 EE.LD.QACC_H.H.32.IP

**Instruction Word Table:**
- Columns labeled as "imm[7]", "011100", "imm[6:0]", and "as[3:0]"
- Values in the table are 0, 011100, imm4[6:0], and as[3:0] respectively.

**Subsection Title:**
Assembler Syntax

**Body Text:**
EE.LD.QACC_H.H.32.IP as -512..508

**Description Section:**
This instruction forces the lower 2 bits of the access address in register `as` to zero and loads 32-bit data from memory to the special register QACC_H[159:128]. After the access is completed, the value in register `as` is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 2.

**Operation Section (with code):**
```
1. QACC_H[159:128] = load32({as[31:2], 0})
2. as[31:0] = as[31:0] + {2imm4[7], imm4[7:0], 2}
```

**Footer Information:**
Espressif Systems
96 ESP32-S3 TRM (Version 1.7)

**Link Texts:**
- GoBack
- Submit Documentation Feedback