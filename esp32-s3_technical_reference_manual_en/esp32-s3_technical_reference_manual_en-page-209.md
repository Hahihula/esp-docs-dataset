**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.133 EE.VMUL.U8.ST.INCP

**Subsection - Instruction Word:**
- 1101000 qy[0] qv[2:0] 1 qz[2:0] qx[1:0] qy[2:1] 0000 as[3:0] 111 qx[2]

**Subsection - Assembler Syntax:**
EE.VMUL.U8.ST.INCP qv, as, qz, qx, qy

**Subsection - Description:**
This instruction performs an unsigned vector multiplication on 8-bit data. Registers qx and qy are the multiplier and the multiplicand respectively. The 16 bit-data results obtained from the calculation is logically right-shifted by the value in special register SAR. Then, the lower 8-bit data of the shift result is written into corresponding segment of register qx.

During the operation, the instruction forces the lower 4 bits of the access address in register as to 0 and stores the value in register qv to memory. After the access, the value in register as is incremented by 16.

**Subsection - Operation:**
- The text contains a series of operations involving registers and their values with specific instructions for each operation step.
  
**Footer Information:**
Espressif Systems
209 ESP32-S3 TRM (Version 1.7)

**Link Texts in Image:**
GoBack, Submit Documentation Feedback