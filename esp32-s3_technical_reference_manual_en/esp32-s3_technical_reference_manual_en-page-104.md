**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Link:**
GoBack

**Section Title:**
1.8.28 EE.LDF.64.XP

**Subsection - Instruction Word Table:**
- fu0[3:0]: 0110
- fu1[3:0]: ad[3:0]
- as[3:0]: 0000

**Subsection Title:**
Assembler Syntax

**Body Text:**
EE.LDF.64.XP fu1, fu0, as, ad

**Subsection - Description:**
This instruction forces the lower 3 bits of the access address in register as to 0, loads 64-bit data from memory, and stores it in order from low bit to high bit to floating-point registers fu0 and fu1. After the access is completed, the value in register as is incremented by the value in register ad.

**Subsection - Operation:**
```
dataIn[63:0] = load64({as[31:3], 3{0}})
fu1 = dataIn[63:32]
fu0 = dataIn[31: 0]
as[31:0] = as[31:0] + ad[31:0]
```