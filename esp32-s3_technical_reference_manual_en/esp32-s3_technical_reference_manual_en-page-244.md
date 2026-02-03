**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.162 EE.VMULAS.U16.ACCX.LD.XP.QUP

**Subsection Headers and Content:**

- **Instruction Word:** 
  - `110000 qu[2:1] qy[0] qsQ[2:0] qu[0] qs1[2:0] qx[1:0] qy[2:1] ad[3:0] as[3:0] 111 qx[2]`

- **Assembler Syntax:** 
  - `EE.VMULAS.U16.ACCX.LD.XP.QUP qu, as, ad, qx, qy, qsQ, qs1`

- **Description:**
  - This instruction divides registers qx and qy into 8 data segments by 16 bits. Then, it performs an unsigned multiply-accumulate operation on the sets of segments respectively. The accumulated result is added to the value in special register ACCX. Then, the sum obtained is saturated and then stored in ACCX.
  - During the operation, the lower 4 bits of the access address in register as are forced to be O, and then the 16-byte data is loaded from the memory to register qu. After the access is completed, the value in register as is incremented by the value in register ad.

- **Additional Information:**
  - At the same time, this instruction also obtains 16-byte unaligned data by concatenating and shifting consecutive aligned data stored in the two registers qsQ0 and qs1 and stores it to qsQ0. The shift byte is stored in special register SAR_BYTE.

**Operation Section (with code examples):**
- `add0[31:0] = qx[ 15: 0] * qy[ 15: 0]`
- `add1[31:0] = qx[ 15: 16] * qy[ 15: 16]`
- `...`
- `add7[31:0] = qx[127:112] * qy[127:112]`
- `sum[40:0] = ACCX[39:0] + ad[31:0]d0[31:0] + ... + ad[31:0]d7[31:0]`

**Additional Operations (with code examples):**
- `ACCX[40:0] = min(max(sum[40:0], 0), 2^{40}-1)`
- `qu[127:0] = load128({as[31:4], 4{0}})`
- `as[31:0] = as[31:0] + ad[31:0]`
- `qsQ0[127:0] = {qs1[127:0], qsQ0[127:0]} >> {SAR_BYTE[3:0] < 3}`

**Footer Information:** 
- Page number and document version:
  - "Espressif Systems"
  - "244 ESP32-S3 TRM (Version 1.7)"
  
**Navigation Links:**
- GoBack
- Submit Documentation Feedback