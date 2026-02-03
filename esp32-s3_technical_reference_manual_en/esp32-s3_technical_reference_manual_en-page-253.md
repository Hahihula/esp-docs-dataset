**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.171 EE.VMULAS.U8.ACCX.LD.IP

**Instruction Word Table:**
- imm16[5:4]: qu[2:1]
- qy[0]: 000
- qu[0]: 110
- qx[1:0]: 111
- qy[2:1]: 111

**Assembler Syntax Table:**
- EE.VMULAS.U8.ACCX.LD.IP qu, as, -512..496, qx, qy

**Description Section:**
This instruction divides registers qx and qy into 16 data segments by 8 bits. Then it performs an unsigned multiply-accumulate operation on the sets of segment respectively. The accumulated result is added to the value in special register ACCX. Then, the sum obtained is saturated and then stored in ACCX.

During the operation, the lower 4 bits of the access address in register as are forced to be O, and then the 16-byte data is loaded from the memory to register qu. After the access is completed, the value in register as is incremented by a 6-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Operation Section:**
```
add0[15:0] = qx[7:0] * qy[7:0]
add1[15:0] = qx[8:0] * qy[15:8]

...
add15[15:0] = qx[127:120] * qy[127:120]

sum[40:0] = ACCX[39:0] + ad[31:0)d0[15:0] + ad[31:0]d1[15:0] + ... + ad[31:0]d15[0]
ACCX[40:0] = min(max(sum[40:0], 0), 2^{40}-1)

qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + {20{imm16[7]},imm16[7:0],4{0}}
```

**Footer Information:**
Espressif Systems
Page 253 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback