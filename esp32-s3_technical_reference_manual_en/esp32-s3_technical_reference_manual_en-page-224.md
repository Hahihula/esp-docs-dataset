**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PE)

**Section Header:**
1.8.148 EE.VMULAS.S.ACCX.LD.IP.QUP

**Instruction Word Table:**
- 0010
- imm16[16:5]
- qu[2:1]
- qy[0]
- qs0[2:0]
- qu[0]
- qs1[2:0]
- qx[1:0]
- qy[2:1]
- imm16[3:0]
- as[3:0]
- 111
- qx[2]

**Assembler Syntax Table:**
- EE.VMULAS.S8.ACCX.LD.IP.QUP, as, imm16, qx, qs0, qs1

**Description Section:**

This instruction divides registers qx and qs into 16 data segments by 8 bits. Then it performs a signed multiply-accumulate operation on the 16 sets of segments respectively. The accumulated result is added to the value in special register ACCX. Then, the sum obtained is saturated and then stored in ACCX.

During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access is completed, the value in register as is incremented by a 6-bit sign-extended constant in the instruction code segment left-shifted by 4.

At the same time, this instruction also obtains 16-byte unaligned data by concatenating and shifting consecutive aligned data stored in the two registers qs0 and qs1 and stores it to qs0. The shift byte is stored in special register SAR_BYTE.

**Operation Section:**

```
addq[15:0] = qx[7:0] * qy[7:0]
add1[15:0] = qx[8:0] * qy[15:8]

...

add15[15:0] = qx[127:120] * qy[127:120]

sum[40:0] = ACCX[39:0] + ad[31:0]d0[15:0] + ad[31:0]d1[15:0] + ... + ad[31:0]d15[15:0]

qu[127:0] = load128({as[31:4], 4{0}})
as[31:0] = as[31:0] + {20imm16[7]}, imm16[7:0], 4{0}}
qs0[127:0] = {qs1[127:0], qs0[127:0]} >> {SAR_BYTE[3:0] << 3}
```