**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.136 EE.VMULAS.S16.ACCX.LD.IP.QUP

**Instruction Word Table:**
- 0000: imm16[5:4] | qu[2:1] | qy[0] | qs0[2:0] | qu[0] | qs1[2:0] | qsx[1:0] | qsx[2:1] | imm16[3:0]
- 111: as[3:0]

**Assembler Syntax:**
EE.VMULAS.S16.ACCX.LD.IP.QUP qu, as, imm16, qx, qy, qs0, qs1

**Description:**
This instruction divides registers qx and qy into 8 data segments by 16 bits. Then it performs a signed multiply-accumulate operation on the sets of segments respectively. The accumulated result is added to the value in special register ACCX.

Then, the sum obtained is saturated and then stored in ACCX.
During the operation, the lower 4 bits of the access address in register as are forced to be 0,
and
then

16-byte data is loaded from the memory to register qu. After the access is completed,

the value in register as is incremented by a 6-bit sign-extended constant in the instruction code segment left-shifted by 4.

At the same time, this instruction also obtains 16-byte unaligned data by concatenating and shifting consecutive aligned data stored in the two registers qs0 and qs1. The shift byte is stored

in special register SAR_BYTE.

**Operation:**
```
addq[31:0] = qx[ 15: 0] * qy[ 15: 0]
add1[31:0] = qx[ 15: 16] * qy[ 31: 16]

...

add7[31:0] = qx[127:112] * qy[127:112]

sum[40:0] = ACCX[39:0] + ad[31:0)d0[31:0] + ad[31:0]d1[31:0] + ... + ad[31:0]d7[31:0]

ACCX[39:0] = min(max(sum[40:0], -2^39), 2^39-1)

qu[127:0] = load128({as[31:4], 4})

as[31:0] = as[31:0] + {20imm16[7], imm16[7:0], 4}

qs0[127:0] = {qs1[127:0], qs0[127:0]} >> SAR_BYTE[3:0]
```