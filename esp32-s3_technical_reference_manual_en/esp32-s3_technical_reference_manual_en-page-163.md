**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.87 EE.VCMP.LT.S8

**Instruction Word Breakdown Table:**
- `10`: qa[2:1]
- `1110`: qa[0]
- `qy[2]`: 1
- `qy[1:0]`: qx
- `qx[2:0]`: 00010100

**Assembler Syntax:**
EE.VCMP.LT.S8 qa, qx, qy

**Description:**
This instruction compares 8-bit vector data. It compares the numerical values of the 16 8-bit data segments in registers qx and qy. If the former is smaller than the latter, it writes 0xFF into the corresponding 8-bit data segment in register qa. Otherwise, it writes 0 to the segment.

**Operation:**
```
qa[7: 0] = (qx[7: 0]<qy[7: 0]) ? 0x{FF} : 0
qa[15: 8] = (qx[15: 8]<qy[15: 8]) ? 0x{FF} : 0
...
qa[127:120] = (qx[127:120]<qy[127:120]) ? 0x{FF} : 0
```