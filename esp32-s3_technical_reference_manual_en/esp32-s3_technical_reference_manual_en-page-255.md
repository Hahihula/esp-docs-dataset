**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.173 EE.VMULAS.U8.ACCX.LD.XP

**Instruction Word Table:**
- qu[2:1]: 001
- qu[0]: 001
- qu[1:0]: 110
- qx[1:0]: 110
- qy[2:1]: ad[3:0]
- qx[2]: as[3:0]

**Assembler Syntax:**
EE.VMULAS.U8.ACCX.LD.XP qu, as, ad, qx, qy

**Description:**
This instruction divides registers qx and qy into 16 data segments by 8 bits. Then it performs an unsigned multiply-accumulate operation on the 16 sets of segments respectively. The accumulated result is added to the value in special register ACCX. Then, the sum obtained is saturated and then stored in ACCX.

During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access is completed, the value in register as is incremented by the value in register ad.

**Operation:**
```
add0[15:0] = qx[7:0] * qy[7:0]
add1[15:0] = qx[8:0] * qy[15:8]
...
add15[15:0] = qx[127:120] * qy[127:120]

sum[40:0] = ACCX[39:0] + ad[31:0]d0[15:0] + ad[31:0]d1[15:0] + ... + ad[31:0]d15[0]
ACCX[40:0] = min(max(sum[40:0], 0), 2^{40}-1)

qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + ad[31:0]
```

**Footer Information:**
Espressif Systems
Page 255 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback