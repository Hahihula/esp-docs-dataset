**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.128 EE.VMUL.U16

**Subheading - Instruction Word:**
- `10` `qz[2:1]` `1110` `qz[0]` `qy[2]` `1` `qy[1:0]` `qx[2:0]` `10100100`

**Subheading - Assembler Syntax:**
- EE.VMUL.U16 qz, qx, qy

**Subheading - Description:**
This instruction performs an unsigned vector multiplication on 16-bit data. Registers qx and qy are the multiplier and the multiplicand respectively. The eight 32-bit data results obtained from the calculation is logically right-shifted by the value in special register SAR. Then, the lower 16-bit data of the shift result is written into corresponding segment of register qz.

**Subheading - Operation:**
- `qz[ 15: 0 ] = (qx[ 15: 0 ] * qy[ 15: 0 ]) >> SAR[5:0]`
- `qz[31: 16] = (qx[31: 16] * qy[31: 16]) >> SAR[5:0]`
- `qz[47: 32] = (qx[47: 32] * qy[47: 32]) >> SAR[5:0]`
- `qz[63: 48] = (qx[63: 48] * qy[63: 48]) >> SAR[5:0]`
- `qz[79: 64] = (qx[79: 64] * qy[79: 64]) >> SAR[5:0]`
- `qz[95: 80] = (qx[95: 80] * qy[95: 80]) >> SAR[5:0]`
- `qz[111: 96] = (qx[111: 96] * qy[111: 96]) >> SAR[5:0]`
- `qz[127:112] = (qx[127:112] * qy[127:112]) >> SAR[5:0]`

**Footer Information:**
Espressif Systems
Page 204 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback