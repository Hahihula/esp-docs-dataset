**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.113 EE.VMIN.S16

**Instruction Word:**
```
10   qa[2:1]  1110   qa[0]   qy[2]  1   qy[1:0]   qx[2:0]   01010100
```

**Assembler Syntax:**
EE.VMIN.S16 qa, qx, qy

**Description:**
This instruction compares numerical values of the eight 16-bit vector data segments in registers qx and qy. The data segment with the smaller value is written into the corresponding 16-bit data segment in register qa.

**Operation (Code Block):**
```
qa[ 15 :   0 ] = (qx[ 15 :  0 ]<=qy[ 15 :  0 ]) ? qx[ 15 :  0 ] : qy[ 15 :  0 ]
qa[ 31 : 16 ] = (qx[ 31 : 16 ]<=qy[ 31 : 16 ]) ? qx[ 31 : 16 ] : qy[ 31 : 16 ]
...
qa[127:112] = (qx[127:112]<=qy[127:112]) ? qx[127:112] : qy[127:112]
```

**Footer Information:**
Espressif Systems
Page Number 189

**Document Version and Feedback Link:**
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback