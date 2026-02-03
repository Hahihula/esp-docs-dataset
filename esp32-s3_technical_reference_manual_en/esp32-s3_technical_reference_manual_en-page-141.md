**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.65 EE.STF.128.IP

**Instruction Word Table:**
- `10010`
- `fv3[3:1]`
- `fvO[3:0]`
- `fv3[0]`
- `fv2[3:1]`
- `fv1[3:0]`
- `imm16f[3:0]`
- `as[3:0]`
- `111`
- `fv2[0]`

**Assembler Syntax Table:**
- `EE.STF.128.IP fv3, fv2, fv1, fvO, as, -128..112`

**Description Section:**
This instruction forces the lower 4 bits of the access address in register as to 0 and stores the 16-byte data concatenated from four floating-point registers fu0, fu1, fu2, and fu3 in order from low bit to high bit to memory. After the access is completed, the value in register as is incremented by 4-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Operation Section:**
```
{fv3, fv2, fv1, fv0} => store128({as[31:4], 4{0}})
as[31:0] = as[31:0] + {24{imm16f[3]}, imm16f[3:0], 4{0}}
```