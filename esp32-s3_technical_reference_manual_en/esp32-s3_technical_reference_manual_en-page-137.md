**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.61 EE.ST.QACC_H.L.128.IP

**Instruction Word Table:**
- `0`: imm16[7]
- `0011010`: imm16[6:0]
- `as[3:0]`: 0100
- `imm16[6:0]`: as[3:0]

**Assembler Syntax Section:**
EE.ST.QACC_H.L.128.IP as, -2048..2032

**Description Section:**
This instruction forces the lower 4 bits of the access address in register as to zero and stores the lower 128 bits in special register QACC_H to memory. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Operation Section:**
```
1   QACC_H[127:0] => store128({as[31:4],4{0}})
2   as[31:0] = as[31:0] + {23{imm4[7]},imm4[7:0],2{0}}
```