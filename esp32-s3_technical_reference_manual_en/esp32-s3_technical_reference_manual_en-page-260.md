**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.178 EE.VMULAS.US.QACC.LD.XP

**Instruction Word Table:**
- qu[2:1] | qy[0]
- 001 | qu[0] 111
- qx[1:0] | qy[2:1] ad[3:0] as[3:0] 111 qx[2]

**Assembler Syntax:**
EE.VMULAS.US.QACC.LD.XP qu, as, ad, qx, qy

**Description:**
This instruction divides registers qx and qy into 16 data segments by 8 bits. The unsigned multiplication result of the 16 sets of segments is added to the corresponding 20-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 20-bit unsigned number and then stored to the corresponding 20-bit data segment in QACC_H and QACC_L.

During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access is completed, the value in register as is incremented by the value in register ad.

**Operation:**
```
QACC_L[ 19: 0 ] = min(QACC_L[ 19: 0 ] + qx[ 7: 0 ] * qy[ 7: 0 ], 2^{20}-1)
QACC_L[ 39: 20 ] = min(QACC_L[ 39: 20 ] + qx[ 15: 8 ] * qy[ 15: 8 ], 2^{w0}-1)

...
QACC_L[159:140] = min(QACC_L[159:140] + qx[63:56] * qy[63:56], 2^{20}-1)
QACC_H[ 19: 0 ] = min(QACC_H[ 19: 0 ] + qx[ 71: 64 ] * qy[ 71: 64 ], 2^{20}-1)
QACC_H[39: 20 ] = min(QACC_H[39: 20 ] + qx[ 79: 72 ] * qy[ 79: 72 ], 2^{20}-1)

...
QACC_H[159:140] = min(QACC_H[159:140] + qx[127:120], 2^{20}-1)
qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + ad[31:0]
```

**Footer Information:**
Espressif Systems
Page 260 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback