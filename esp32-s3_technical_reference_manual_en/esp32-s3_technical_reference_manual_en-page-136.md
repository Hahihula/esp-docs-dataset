**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.60 EE.ST.QACC_H.H.32.IP

**Instruction Word Table:**
- Instruction Word:
  - O imm[7] 0100100 imm4[6:0] as[3:0] 0100
- Assembler Syntax:
  - EE.ST.QACC_H.H.32.IP as, -512..508

**Description Section:**
This instruction forces the lower 2 bits of the access address in register as to 0 and stores the upper 32 bits in special register QACC_H to memory. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 2.

**Operation Section:**
1. QACC_H[159:128] => store32({as[31:2],2{0}})
2. as[31:0] = as[31:0] + {23{imm4[7]},imm4[7:0],2{0}}