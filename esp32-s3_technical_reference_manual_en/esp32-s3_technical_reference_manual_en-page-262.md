**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.180 EE.VMULAS.U8.QACC.LDBC.INCP

**Instruction Word Table:**
- qu[2]
- qy[2]
- qu[0]
- qy[0]
- qx[1:0]
- as[3:0]
- 0100

**Assembler Syntax:**
EE.VMULAS.U8.QACC.LDBC.INCP qu, as, qx, qy

**Description:**
This instruction divides registers qx and qy into 16 data segments by 8 bits. Then, the unsigned multiplication result of the 16 sets of segments is added to the corresponding 20-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 20-bit unsigned number and then stored to the corresponding 20-bit data segment in QACC_H and QACC_L.

At the same time, this instruction loads 8-bit data from memory at the address given by the access register as and broadcasts it to the 16 8-bit data segments in register qu. After the access, the value in register as is incremented by 1.

**Operation:**
```
QACC_L[ 19: 0 ] = min(QACC_L[ 19: 0 ] + qx[ 7: 0 ] * qy[ 7: 0 ], 2^{20}-1)
QACC_L[ 39: 20 ] = min(QACC_L[ 39: 20 ] + qx[ 15: 8 ] * qy[ 15: 8 ], 2^{w0}-1)

...
QACC_L[159:140] = min(QACC_L[159:140] + qx[63:56] * qy[63:56], 2^{20}-1)
QACC_H[ 19: 0 ] = min(QACC_H[ 19: 0 ] + qx[71:64] * qy[71:64], 2^{20}-1)
QACC_H[39:20] = min(QACC_H[39:20] + qx[79:72] * qy[79:72], 2^{20}-1)

QACC_H[159:140] = min(QACC_H[159:140] + qx[127:120] * qy[127:120], 2^{20}-1)
qu[127:0] = {16[load8(as[31:0])}}
as[31:0] = as[31:0] + 1
```

**Footer Information:**
Espressif Systems  
Page Number: 262  
Document Version: ESP32-S3 TRM (Version 1.7)