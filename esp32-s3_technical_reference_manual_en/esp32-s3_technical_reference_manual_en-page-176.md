**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.100 EE.VLDBEC.8

**Subsection - Instruction Word:**
- 11
- qu[2:1] = 1101
- qu[0] = 0111011
- as[3:0] = 0100

**Subsection - Assembler Syntax:**
EE.VLDBEC.8 qu, as

**Subsection - Description:**
This instruction loads 8-bit data from memory at the address given by the access register `as` and broadcasts it to the 16 8-bit data segments in register `qu`.

**Subsection - Operation:**
```
qu[127:0] = {16(load8(as[31:0]))}
```