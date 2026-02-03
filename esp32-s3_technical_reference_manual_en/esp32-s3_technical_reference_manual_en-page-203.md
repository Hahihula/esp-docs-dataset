**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.127 EE.VMUL.S8.ST.INCP

**Instruction Word Table:**
- 1100101
- qy[0]
- qv[2:0]
- O
- qz[2:0]
- qx[1:0]
- qy[2:1]
- 0011
- as[3:0]
- 111
- qx[2]

**Assembler Syntax:**
EE.VMUL.S8.ST.INCP qv, as, qz, qx, qy

**Description:**
This instruction performs a signed vector multiplication on 8-bit data. Registers qx and qy are the multiplier and the multiplicand respectively. The 16 bit-data results obtained from the calculation is arithmetically right-shifted by the value in special register SAR. Then, the lower 8-bit data of the shift result is written into corresponding segment of register qx.

During the operation, the instruction forces the lower 4 bits of the access address in register as to 0 and stores the value in register qv to memory. After the access, the value in register as is incremented by 16.

**Operation:**
- Diagram showing various operations with different values for qx, qy, and qz registers.
- Example operation sequence:
  - `qv[127:0] = store128({as[31:4], 4{0}})`
  - `as[31:0] = as[31:0] + 16`

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)