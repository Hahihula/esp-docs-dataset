**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
18.74 EE.VMULAS.U8.ACCX.LD.XP.QUP

**Subsection - Instruction Word Table:**
- qu[2:1] : qy[0]
- qs0[2:0] : qu[0]
- qs1[2:0] : qs0[2:0]
- qx[1:0] : qs1[2:0]
- qy[2:1] : ad[3:0]
- as[3:0] : as[3:0]
- 111
- qx[2]

**Subsection - Assembler Syntax:**
EE.VMULAS.U8.ACCX.LD.XP.QUP qu, as, ad, qx, qy, qs0, qs1

**Subsection - Description:**
This instruction divides registers qx and qy into 16 data segments by 8 bits. Then, it performs an unsigned multiply-accumulate operation on the 16 sets of segments respectively. The accumulated result is added to the value in special register ACCX. Then, the sum obtained is saturated and then stored in ACCX.

During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access is completed, the value in register as is incremented by the value in register ad.
At the same time, this instruction also obtains 16-byte unaligned data by concatenating and shifting consecutive aligned data stored in the two registers qs0 and qs1 and stores it to qs0. The shift byte is stored in special register SAR_BYTE.

**Subsection - Operation:**
```
addq[15:0] = qx[7:0] * qy[7:0]
addq[15:0] = qx[8:0] * qy[15:8]

...

addq[15:0] = qx[127:120] * qy[127:120]
sum[40:0] = ACCX[39:0] + ad[31:0]d15:0] + ... + ad[31:0)d15:0]

ACCX[40:0] = min(max(sum[40:0], 0), 2^40-1)

qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + ad[31:0]

qs0[127:0] = {qs1[127:7], qs0[127: 0]} >> {SAR_BYTE[3:0] << 3}
```