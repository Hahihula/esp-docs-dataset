**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.125 EE.VMUL.S8

**Instruction Word Table:**
- 10
- qz[2:1] 1110
- qz[0] qy[2]
- 1
- qy[1:0] qx[2:0]
- qx[0] 10010100

**Subheader - Assembler Syntax:**
EE.VMUL.S8 qz, qx, qy

**Description Section:**
This instruction performs a signed vector multiplication on 8-bit data. Registers qx and qy are the multiplier and the multiplicand respectively. The 16 bit-data results obtained from the calculation is arithmetically right-shifted by the value in special register SAR. Then, the lower 8-bit data of the shift result is written into corresponding segment of register qz.

**Operation Section:**
- qz[7:0] = (qx[7:0] * qx[7:0]) >> SAR[5:0]
- qz[15:8] = (qx[15:8] * qx[15:8]) >> SAR[5:0]
- qz[23:16] = (qx[23:16] * qx[23:16]) >> SAR[5:0]
- qz[31:24] = (qx[31:24] * qx[31:24]) >> SAR[5:0]
- qz[39:32] = (qx[39:32] * qx[39:32]) >> SAR[5:0]
- qz[47:40] = (qx[47:40] * qx[47:40]) >> SAR[5:0]
- qz[55:48] = (qx[55:48] * qx[55:48]) >> SAR[5:0]
- qz[63:56] = (qx[63:56] * qx[63:56]) >> SAR[5:0]
- qz[71:64] = (qx[71:64] * qx[71:64]) >> SAR[5:0]
- qz[79:72] = (qx[79:72] * qx[79:72]) >> SAR[5:0]
- qz[87:80] = (qx[87:80] * qx[87:80]) >> SAR[5:0]
- qz[95:88] = (qx[95:88] * qx[95:88]) >> SAR[5:0]
- qz[103:96] = (qx[103:96] * qx[103:96]) >> SAR[5:0]
- qz[111:104] = (qx[111:104] * qx[111:104]) >> SAR[5:0]
- qz[119:112] = (qx[119:112] * qx[119:112]) >> SAR[5:0]
- qz[127:120] = (qx[127:120] * qx[127:120]) >> SAR[5:0]

**Footer Information:**
Espressif Systems
Page 201 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback