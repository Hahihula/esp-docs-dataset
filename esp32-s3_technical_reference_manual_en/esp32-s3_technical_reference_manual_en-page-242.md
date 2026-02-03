**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PE)

**Section Header:**
1.8.160 EE.VMULAS.U16.ACCX.LD.IP.QUP

**Subheader - Instruction Word:**
- 0100 imm16[5:4] qu[2:1] qy[0] qs0[2:0] qu[0] qs1[2:0] qx[1:0] qy[2:1] imm16[3:0] as[3:0] 111 qx[2]

**Subheader - Assembler Syntax:**
EE.VMULAS.U16.ACCX.LD.IP.QUP qu, as, imm16, qx, qs0, qs1

**Subheader - Description:**
This instruction divides registers qx and qy into 8 data segments by 16 bits. Then it performs a signed multiply-accumulate operation on the sets of segments respectively. The accumulated result is added to the value in special register ACCX.

During the operation, the lower 4 bits of the access address in register qs are forced to be O, and then the 16-byte data is loaded from the memory to register qx. After the access is completed, the value in register as is incremented by a 6-bit sign-extended constant in the instruction code segment left-shifted by 4.

At the same time, this instruction also obtains 16-byte unaligned data by concatenating and shifting consecutive aligned data stored in the two registers qs0 and qs1. The shift byte is stored in special register SAR_BYTE.

**Subheader - Operation:**
- addq[31:0] = qx[ 15: 0] * qy[ 15: 0]
- add1[31:0] = qx[ 31: 16] * qy[ 31: 16]
- ...
- add7[31:0] = qx[127:112] * qy[127:112]
- sum[40:0] = ACCX[39:0] + ad[31:0)d0[31:0] + ad[31:0]d1[31:0] + ... + ad[31:0]d7[31:0]
- ACCX[40:0] = min(max(sum[40:0], 0), 2^{40}-1)
- qu[127:0] = load128({as[31:4], 4{0}})
- as[31:0] = as[31:0] + {20imm16[7]:, imm16[7:0], 4{0}}
- qs0[127:0] = {qs1[127:0], qs0[127:0]} >> SAR_BYTE[3:0]

**Footer Information:**
Espressif Systems
Page Number: 242
Document Title: ESP32-S3 TRM (Version 1.7)
Link Texts:
- Submit Documentation Feedback