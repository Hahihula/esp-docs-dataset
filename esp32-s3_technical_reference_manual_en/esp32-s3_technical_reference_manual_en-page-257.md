**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.175 EE.VMULAS.U8.QACC

**Instruction Word Table:**
- Instruction Word: `000010100`
- qy[2]: `1`
- qx[1:0]: `1`
- qx[2:0]: `11000100`

**Assembler Syntax:**
```
EE.VMULAS.U8.QACC qx, qy
```

**Description:**
This instruction divides registers qx and qy into 16 data segments by 8 bits. The unsigned multiplication result of the 16 sets of segments is added to the corresponding 20-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 20-bit unsigned number and then stored to the corresponding 20-bit data segment in QACC_H and QACC_L.

**Operation:**
```
QACC_L[19:0] = min(QACC_L[19:0] + qx[7:0] * qy[7:0], 2^{20}-1)
QACC_L[39:20] = min(QACC_L[39:20] + qx[15:8] * qy[15:8], 2^{w0}-1)
...
QACC_L[159:140] = min(QACC_L[159:140] + qx[63:56] * qy[63:56], 2^{20}-1)
QACC_H[19:0] = min(QACC_H[19:0] + qx[71:64] * qy[71:64], 2^{20}-1)
QACC_H[39:20] = min(QACC_H[39:20] + qx[79:72] * qy[79:72], 2^{20}-1)
...
QACC_H[159:140] = min(QACC_H[159:140] + qx[127:120] * qy[127:120], 2^{20}-1)
```

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)