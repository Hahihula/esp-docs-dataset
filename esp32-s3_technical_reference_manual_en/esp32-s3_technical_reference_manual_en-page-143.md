**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Subtitle:**
1.8.67 EE.STF.64.IP

**Instruction Word Table:**
- 111000
- imm8[7:6]
- fv0[3:0]
- imm8[5:2]
- fv1[3:0]
- O11
- imm8[0]
- as[3:0]
- 111
- imm8[1]

**Assembler Syntax Section Title:**
Assembler Syntax

**Assembler Syntax Content:**
EE.STF.64.IP fv1, fv0, as, imm8

**Description Section Title:**
Description

**Description Text:**
This instruction forces the lower 3 bits of the access address in register `as` to 0 and stores the 64-bit data concatenated from two floating-point registers `fu0` and `fu1` in order from low bit to high bit to memory. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 3.

**Operation Section Title:**
Operation

**Operation Text with Code Block:**
```
{fv1, fv0} => store64({as[31:3],3,0})
as[31:0] = as[31:0] + {21{imm8[7]},imm8[7:0],3,0}
```