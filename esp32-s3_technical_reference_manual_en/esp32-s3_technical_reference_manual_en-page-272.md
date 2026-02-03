**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PEIE)

**Section Header:**
1.8.190 EE.VSMULAS.S8.QACC.LD.INCP

**Instruction Word Table:**
- 111000
- qu[2:1]
- qy[0]
- O1
- sel16[0]
- qu[0]
- sel16[3:1]
- qx[1:0]
- qy[2:1]
- 1100
- as[3:0]
- 111
- qx[2]

**Assembler Syntax:**
EE.VSMULAS.S8.QACC.LD.INCP, qu, as, qx, qy, sel16

**Description:**
This instruction selects one out of the 16 8-bit data segments in register qy according to immediate number sel16 and performs a signed multiplication on it and the 16 8-bit data segments in register qx respectively. The 16 results obtained are added to the corresponding 20-bit data segment in special registers QACC_H and QACC_L respectively, Then, the result is saturated to a 20-bit signed number and then stored to the corresponding 20-bit data segment in QACC_H and QACC_L.

During the operation, the lower 4 bits of the access address in register as are forced to be O, and then the 16-byte data is loaded from the memory to register qu. After the access, the value in register as is incremented by 16.

**Operation:**
```
temp[7:0] = qy[sel16*8+7:sel16*8]
QACC_L[ 19 : 0 ] : m = min(max(QACC_L[ 19 : 0 ] + qx[ 7 : 0 ] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_L[ 39 : 20 ] : m = min(max(QACC_L[ 39 : 20 ] + qx[ 15 : 8 ] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_L[ 59 : 40 ] : m = min(max(QACC_L[ 59 : 40 ] + qx[ 23 : 16 ] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_L[ 79 : 60 ] : m = min(max(QACC_L[ 79 : 60 ] + qx[ 31 : 24 ] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_L[ 99 : 80 ] : m = min(max(QACC_L[ 99 : 80 ] + qx[ 39 : 32 ] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_L[119:100] : m = min(max(QACC_L[119:100] + qx[ 47 : 40 ] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_L[139:120] : m = min(max(QACC_L[139:120] + qx[ 55 : 48 ] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_L[159:140] : m = min(max(QACC_L[159:140] + qx[ 63 : 56 ] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_H[ 19 : 0 ] : m = min(max(QACC_H[ 19 : 0 ] + qx[ 71 : 64 ] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_H[ 39 : 20 ] : m = min(max(QACC_H[ 39 : 20 ] + qx[ 79 : 72 ] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_H[ 59 : 40 ] : m = min(max(QACC_H[ 59 : 40 ] + qx[ 87 : 80 ] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_H[ 79 : 60 ] : m = min(max(QACC_H[ 79 : 60 ] + qx[ 95 : 88 ] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_H[ 99 : 80 ] : m = min(max(QACC_H[ 99 : 80 ] + qx[103 : 96 ] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_H[119:100] : m = min(max(QACC_H[119:100] + qx[111:104] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_H[139:120] : m = min(max(QACC_H[139:120] + qx[119:112] * temp[7:0], -2^{19}), 2^{19}-1)
QACC_H[159:140] : m = min(max(QACC_H[159:140] + qx[127:120] * temp[7:0], -2^{19}), 2^{19}-1)
```

**Footer Information:**
Espressif Systems
Page number: 272
Document version information (Version 1.7)