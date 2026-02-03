**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
18.156 EE.VMULAS.S8.QACC.LDBC.INCP

**Instruction Word:**
- 101 qu[2] O111 q[1] qy[2] qu[0] qy[1:0] qx[2:0] as[3:0] 0100

**Assembler Syntax:**
EE.VMULAS.S8.QACC.LDBC.INCP qu, as, qx, qy

**Description:**
This instruction divides registers qx and qy into 16 data segments by 8 bits. Then, the signed multiplication result of the 16 sets of segments is added to the corresponding 20-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 20-bit signed number and then stored to the corresponding 20-bit data segment in QACC_H and QACC_L.

At the same time, this instruction loads 8-bit data from memory at the address given by the access register as and broadcasts it to the 16 8-bit data segments in register qu. After the access, the value in register as is incremented by 1.

**Operation:**
```
QACC_L[ 19: 0 ] = min(max(QACC_L[ 19: 0 ] + qx[ 7: 0 ] * qy[ 7: 0 ], -2^{19}), 2^{19}-1)
QACC_L[ 39: 20 ] = min(max(QACC_L[ 39: 20 ] + qx[ 15: 8 ] * qy[ 15: 8 ], -2^{19}), 2^{19}-1)
QACC_L[ 59: 40 ] = min(max(QACC_L[ 59: 40 ] + qx[ 23: 16 ] * qy[ 23: 16 ], -2^{19}), 2^{19}-1)
QACC_L[ 79: 60 ] = min(max(QACC_L[ 79: 60 ] + qx[ 31: 24 ] * qy[ 31: 24 ], -2^{19}), 2^{19}-1)
QACC_L[ 99: 80 ] = min(max(QACC_L[ 99: 80 ] + qx[ 39: 32 ] * qy[ 39: 32 ], -2^{19}), 2^{19}-1)
QACC_L[119:100] = min(max(QACC_L[119:100] + qx[ 47: 40 ] * qy[ 47: 40 ], -2^{19}), 2^{19}-1)
QACC_L[139:120] = min(max(QACC_L[139:120] + qx[ 55: 48 ] * qy[ 55: 48 ], -2^{19}), 2^{19}-1)
QACC_L[159:140] = min(max(QACC_L[159:140] + qx[ 63: 56 ] * qy[ 63: 56 ], -2^{19}), 2^{19}-1)
QACC_H[ 19: 0 ] = min(max(QACC_H[ 19: 0 ] + qx[ 71: 64 ] * qy[ 71: 64 ], -2^{19}), 2^{19}-1)
QACC_H[39: 20 ] = min(max(QACC_H[ 39: 20 ] + qx[ 79: 72 ] * qy[ 79: 72 ], -2^{19}), 2^{19}-1)
QACC_H[59: 40 ] = min(max(QACC_H[ 59: 40 ] + qx[ 87: 80 ] * qy[ 87: 80 ], -2^{19}), 2^{19}-1)
QACC_H[ 79: 60 ] = min(max(QACC_H[ 79: 60 ] + qx[ 95: 88 ] * qy[ 95: 88 ], -2^{19}), 2^{19}-1)
QACC_H[ 99: 80 ] = min(max(QACC_H[ 99: 80 ] + qx[103: 96 ] * qy[103: 96 ], -2^{19}), 2^{19}-1)
QACC_H[119:100] = min(max(QACC_H[119:100] + qx[111:104 ] * qy[111:104 ], -2^{19}), 2^{19}-1)
QACC_H[139:120] = min(max(QACC_H[139:120] + qx[119:112 ] * qy[119:112 ], -2^{19}), 2^{19}-1)
QACC_H[159:140] = min(max(QACC_H[159:140] + qx[127:120 ] * qy[127:120 ], -2^{19}), 2^{19}-1)
```

**Footer Information:**
Espressif Systems
Page number: 236
Document version and feedback link:
ESP32-S3 TRM (Version 1.7) Submit Documentation Feedback