**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.183 EE.VPRELU.S8

**Subheader - Instruction Word:**
```
10   |  qz[2:1]  1100  |  qz[0]  |  qy[2]  |  qy[1:0]  |  qx[2:0]  |  ay[3:0]  |  0100
```

**Subheader - Assembler Syntax:**
EE.VPRELU.S8 qz, qx, qy, ay

**Subheader - Description:**
This instruction divides register qx into 16 data segments by 8 bits. If the value of the segment is not greater than 0, it will be multiplied by the value of the corresponding 8-bit segment in register qy and right-shifted by the lower 5-bit value in register qy, and then the calculated result will be assigned to the corresponding 8-bit data segment in register qz. Otherwise, the value of the segment in qx will be assigned to qz.

**Subheader - Operation:**
```
qz[7:0] = (qx[7:0] <= 0) ? (qx[7:0] * qy[7:0]) >> ay[4:0] : qx[7:0]
qz[15:8] = (qx[15:8] <= 0) ? (qx[15:8] * qy[15:8]) >> ay[4:0] : qx[15:8]
...
qz[127:120] = (qx[127:120] <= 0) ? (qx[127:120] * qy[127:120]) >> ay[4:0] : qx[127:120]
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback