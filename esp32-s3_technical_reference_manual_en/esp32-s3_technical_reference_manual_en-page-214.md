**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.138 EE.VMULAS.S16.ACCX.LD.XP.QUP

**Instruction Word Table:**
- qu[2:1] : qy[0]
- qs0[2:0] : qs1[2:0]
- qu[0]  : qs1[0]
- qs1[2:0] : qs0
- qx[1:0] : ad[3:0]
- as[3:0] : qx[2]

**Assembler Syntax:**
EE.VMULAS.S16.ACCX.LD.XP.QUP qu, as, ad, qx, qy, qs0, qs1

**Description:**
This instruction divides registers qx and qy into 8 data segments by 16 bits. Then, it performs a signed multiply-accumulate operation on the sets of segments respectively. The accumulated result is added to the value in special register ACCX. Then, the sum obtained is saturated and then stored in ACCX.

During the operation, the lower 4 bits of the access address in register as are forced to be O, and then the 16-byte data is loaded from the memory to register qu. After the access is completed, the value in register as is incremented by the value in register ad.
At the same time, this instruction also obtains 16-byte unaligned data by concatenating and shifting consecutive aligned data stored in the two registers qs0 and qs1 and stores it to qs0. The shift byte is stored in special register SAR_BYTE.

**Operation:**
```
add0[31:0] = qx[ 15: 0] * qy[ 15: 0]
add1[31:0] = qx[ 16: 0] * qy[ 31: 16]

...

add7[31:0] = qx[127:112] * qy[127:112]

sum[40:0] = ACCX[39:0] + ad[31:0)d0[31:0] + ad[31:0]d1[31:0] + ... + ad[31:0]d7[31:0]

ACCX[39:0] = min(max(sum[40:0], -2^39), 2^39-1)

qu[127:0] = load128({as[31:4], 4, 0})

as[31:0] = as[31:0] + ad[31:0]

qs0[127:0] = {qs1[127: 0], qs0[127: 0]} >> {SAR_BYTE[3:0] << 3}
```