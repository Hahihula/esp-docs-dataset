**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.24 EE.LD.UA_STATE.IP

**Instruction Word Breakdown Table:**
- 0: imm16[7]
- 0: 010000
- 0: imm16[6:0]
- 3: as[3:0]
- 0: 0100

**Subsection Title:**
Assembler Syntax

**Syntax Description:**
EE.LD.UA_STATE.IP as, -2048..2032

**Description Section:**
This instruction forces the lower 4 bits of the access address in register as to zero and loads 16-byte data from memory to the special register UA_STATE. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Operation Section:**
```
UA_STATE[127:0] = lod128({as[31:4],4{0}})
as[31:0] = as[31:0] + {20{imm16[7]},imm16[7:0],4{0}}
```

**Footer Information:**
Espressif Systems
Page Number 100

**Document Version Note:**
ESP32-S3 TRM (Version 1.7)

**Link Texts:**
- GoBack
- Submit Documentation Feedback