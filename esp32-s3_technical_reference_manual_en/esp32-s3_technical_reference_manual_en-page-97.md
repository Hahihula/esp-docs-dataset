**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.21 EE.LD.QACC_H.L.128.IP

**Instruction Word Table:**
- `imm16[7]`
- `0001100`
- `imm16[6:0]`
- `as[3:0]`
- `0100`

**Subsection Title:**
Assembler Syntax

**Body Text:**
EE.LD.QACC_H.L.128.IP as, -2048..2032

**Description Section:**
This instruction forces the lower 4 bits of the access address in register as to zero and loads 16-byte data from memory to the special register QACC_H[127:0]. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Operation Section (with code example):**
```
1   QACC_H[127: 0] = load128({as[31:4], 4{0}})
2   as[31:0] = as[31:0] + {20imm16[7]}, imm16[7:0], 4{0}}
```

**Footer Information:**
Espressif Systems
97 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback