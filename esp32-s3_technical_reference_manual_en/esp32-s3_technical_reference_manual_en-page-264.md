**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.182 EE.VPRELU.S16

**Subheader - Instruction Word:**
- 10
- qz[2:1]
- 1100
- qz[0]
- qy[2]
- 0
- qy[1:0]
- qx[2:0]
- ay[3:0]
- O100

**Subheader - Assembler Syntax:**
EE.VPRELU.S16 qz, qx, qy, ay

**Subheader - Description:**
This instruction divides register qx into 8 data segments by 16 bits. If the value of the segment is not greater than 0, it will be multiplied by the value of the corresponding 16-bit segment in register qy right-shifted by the lower 6-bit value in register ay, and then the result obtained will be assigned to the corresponding 16-bit data segment in register qx. Otherwise, the value of the segment in qx will be assigned to qx.

**Subheader - Operation:**
```
qz[ 15: 0 ] = (qx[ 15: 0]<=0) ? (qx[ 15: 0] * qy[ 15: 0]) >> ay[5:0] : qx[ 15: 0]
qz[ 31: 16 ] = (qx[ 31: 16]<=0) ? (qx[ 31: 16] * qy[ 31: 16]) >> ay[5:0] : qx[ 31: 16]
...
qz[127:112] = (qx[127:112]<=0) ? (qx[127:112] * qy[127:112]) >> ay[5:0] : qx[127:112]
```

**Footer Information:**
Espressif Systems
Page 264 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback