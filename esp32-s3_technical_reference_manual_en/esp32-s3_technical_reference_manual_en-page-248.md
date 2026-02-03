**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.166 EE.VMULAS.U16.QACC.LD.XP

**Instruction Word Table:**
- qu[2:1]: 001
- qu[0]: 001
- 101
- qx[1:0]: 001
- qy[2:1]: ad[3:0]
- as[3:0]: a s [3:0]
- qx[2]: 111

**Assembler Syntax:**
EE.VMULAS.U16.QACC.LD.XP qu, as, ad, qx, qy

**Description:**
This instruction divides registers qx and qy into 8 data segments by 16 bits. Then the unsigned multiplication result of the 8 sets of segments is added to the corresponding 40-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 40-bit unsigned number, then stored to the corresponding 40-bit data segment in QACC_H and QACC_L.

During the operation, lower 4 bits of access address in register as are forced to be O, and then the 16-byte data is loaded from memory into register qu. After accessing completed, value in register as incremented by the value in register ad

**Operation:**
```
QACC_L[39:0] = min(QACC_L[39:0] + qx[15:0] * qy[15:0], 2^{40}-1)
QACC_L[79:40] = min(QACC_L[79:40] + qx[31:16] * qy[31:16], 2^{40}-1)
...
QACC_L[159:120] = min(QACC_L[159:120] + qx[63:48] * qy[63:48], 2^{40}-1)
QACC_H[39:0] = min(QACC_H[39:0] + qx[79:64] * qy[79:64], 2^{40}-1)
QACC_H[79:40] = min(QACC_H[79:40] + qx[95:80] * qy[95:80], 2^{40}-1)
...
QACC_H[159:120] = min(QACC_H[159:120] + qx[127:112] * qy[127:112], 2^{40}-1)

qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + ad[31:0]
```

**Footer Information:**
Espressif Systems
Page 248 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback