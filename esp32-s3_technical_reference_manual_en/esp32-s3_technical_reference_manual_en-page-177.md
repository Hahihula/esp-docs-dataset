**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.101 EE.VLDBEC.8.IP

**Instruction Word Breakdown Table:**
- `qu[2:1]`: 0101
- `qu[0]`: 0
- `imm1[6:0]`: 
- `as[3:0]`: 0100

**Assembler Syntax:**
EE.VLDBEC.8.IP qu, as, 0..127

**Description:**
This instruction loads 8-bit data from memory at the address given by the access register `as` and broadcasts it to the 16 8-bit data segments in register `qu`. After the access is completed, the value in register `as` is incremented by a 7-bit unsigned-extended constant in the instruction code segment.

**Operation:**
```
qu[127:0] = {16[load8(as[31:0])]}
as[31:0] = as[31:0] + {25{0},imm1[6:0]}
```