**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.147 EE.VMULAS.S8.ACCX.LD.IP

**Instruction Word Table:**
- imm16[5:4]
- qu[2:1]
- qy[0]
- 000
- qu[0]
- 010
- qx[1:0]
- qy[2:1]
- imm16[3:0]
- as[3:0]
- qx[2]

**Assembler Syntax:**
EE.VMULAS.S8.ACCX.LD.IP qu, as, -512..496, qx, qy

**Description:**
This instruction divides registers qx and qy into 16 data segments by 8 bits. Then it performs a signed multiply-accumulate operation on the sets of segment respectively. The accumulated result is added to the value in special register ACCX. Then, the sum obtained is saturated and then stored in ACCX.

During the operation, the lower 4 bits of the access address in register as are forced to be O, and then the 16-byte data is loaded from the memory to register qu. After the access is completed, the value in register as is incremented by a 6-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Operation:**
```
add0[15:0] = qx[7:0] * qy[7:0]
add1[15:0] = qx[15:8] * qy[15:8]
...
add15[15:0] = qx[127:120] * qy[127:120]

sum[40:0] = ACCX[39:0] + ad[31:0)d0[15:0] + ad[31:0]d1[15:0] + ... + ad[31:0]d15[15:0]

qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + {20{imm16[7]},imm16[7]:0,4{0}}
```