**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.139 EE.VMULAS.S16.QACC

**Instruction Word:**
000110100 | qy[2] 1 | qy[1:0] | qx[2:0] | 10000100

**Assembler Syntax:**
EE.VMULAS.S16.QACC qx, qy

**Description:**
This instruction divides registers qx and qy into 8 data segments by 16 bits. Then, the signed multiplication result of 8 sets of segments is added to the corresponding 40-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 40-bit signed number and then stored to the corresponding 40-bit data segment in QACC_H and QACC_L.

**Operation:**
```
QACC_L[39:0] = min(max(QACC_L[39:0], 0) + qx[15:0], 0) * qy[15:0], -2^39), 
               2^39-1

QACC_L[79:40] = min(max(QACC_L[79:40], qx[31:16]) * qy[31:16], -2^39), 
                2^39-1

QACC_L[119:80] = min(max(QACC_L[119:80], qx[47:32]) * qy[47:32], -2^39), 
                 2^39-1

QACC_L[159:120] = min(max(QACC_L[159:120], qx[63:48]) * qy[63:48], -2^39), 
                  2^39-1

QACC_H[39:0] = min(max(QACC_H[39:0], qx[79:64]) * qy[79:64], -2^39), 
               2^39-1

QACC_H[79:40] = min(max(QACC_H[79:40], qx[95:80]) * qy[95:80], -2^39), 
                2^39-1

QACC_H[119:80] = min(max(QACC_H[119:80], qx[111:96]) * qy[111:96], -2^39), 
                 2^39-1

QACC_H[159:120] = min(max(QACC_H[159:120], qx[127:112]) * qy[127:112], -2^39), 
                  2^39-1
```

**Footer Information:**
Espressif Systems  
Page Number: 215  
Document Title: ESP32-S3 TRM (Version 1.7)  
Link Texts:
- Submit Documentation Feedback