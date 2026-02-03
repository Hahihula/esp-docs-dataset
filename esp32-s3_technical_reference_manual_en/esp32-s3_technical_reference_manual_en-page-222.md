**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.146 EE.VMULAS.SB.ACCX

**Instruction Word Table:**
- Instruction Word: `000110100`
- qy[2]: `0`
- qy[1:0]: `0`
- qx[2:0]: `11000100`

**Assembler Syntax Section:**
- Title: Assembler Syntax
- Content: EE.VMULAS.S8.ACCX qx, qy

**Description Section:**
- Description:
  - This instruction divides registers qx and qy into 16 data segments by 8 bits. Then, it performs a signed multiply-accumulate operation on the 16 sets of segments respectively.
  - The accumulated result is added to the value in special register ACCX.
  - Then, the sum obtained is saturated and then stored in ACCX.

**Operation Section:**
- Operation:
  ```
  add0[15:0] = qx * qy[7: 0]
  add1[15:0] = qx * qy[8: 0]
  ...
  add15[15:0] = qx[127:120] * qy[127:120]
  sum[40:0] = ACCX[39:0] + ad[31:0)d0[15:0] + ad[31:0)d1[15:0] + ... + ad[31:0)d15[15:0]
  ACCX[39:0] = min(max(sum[40:0], -2^39), 2^39-1)
  ```

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)