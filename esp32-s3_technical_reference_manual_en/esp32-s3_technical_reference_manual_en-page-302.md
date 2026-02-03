**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.219 ST.QR

**Instruction Word Breakdown Table:**
- qs[2:1]: 1101
- qs[0]: 110
- imm[3:0]: 
- as[3:0]: 0100

**Subsection Title:**
Assembler Syntax

**Body Text (Syntax):**
LD.QR qs, as, imm, -128..112

**Description Section:**
This instruction stores 128 bits from the source QR register qs to memory.

**Operation Section:**
```
qs => store128(as + imm)
```