**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.142 EE.VMULAS.S16.QACC.LD.XP

**Instruction Word Table:**
- qu[2:1]: 001
- qy[0]: 001
- qu[0]: 001
- qx[1:0]: 001
- qy[2:1]: ad[3:0]
- as[3:0]: 111
- qx[2]

**Assembler Syntax:**
EE.VMULAS.S16.QACC.LD.XP qu, as, ad, qx, qy

**Description:**
This instruction divides registers qx and qy into 8 data segments by 16 bits. Then the signed multiplication result of 8 sets of segments is added to the corresponding 40-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 40-bit signed number and then stored to the corresponding 40-bit data segment in QACC_H and QACC_L.

During the operation, the lower 4 bits of the access address in register as are forced to be O, and then the 16-byte data is loaded from the memory to register qu. After the access is completed, the value in register as is incremented by the value in register ad.

**Operation:**
```
QACC_L[39:0] = min(max(QACC_L[39:0] + qx[15: 0] * qy[15: 0], -2^39), QACC_L-1)
QACC_L[79:40] = min(max(QACC_L[79:40] + qx[31:16] * qy[31:16], -2^39), QACC_L-1)
QACC_L[119:80] = min(max(QACC_L[119:80] + qx[47:32] * qy[47:32], -2^39), QACC_L-1)
QACC_L[159:120] = min(max(QACC_L[159:120] + qx[63:48] * qy[63:48], -2^39), QACC_L-1)

QACC_H[39:0] = min(max(QACC_H[39:0] + qx[79:64] * qy[79:64], -2^39), QACC_H-1)
QACC_H[79:40] = min(max(QACC_H[79:40] + qx[95:80] * qy[95:80], -2^39), QACC_H-1)
QACC_H[119:80] = min(max(QACC_H[119:80] + qx[111:96] * qy[111:96], -2^39), QACC_H-1)
QACC_H[159:120] = min(max(QACC_H[159:120] + qx[127:112] * qy[127:112], -2^39), QACC_H-1)

qu[127:0] = load128({as[31:4], 4{0}})
as[31:6] = as[31:0] + ad[31:0]
```