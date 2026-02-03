**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.83 EE.VCMP.GT.S32

**Subsection - Instruction Word:**
- 10 qa[2:1] 1110 qa[0] 0 qy[2] 0 qx[1:0] 11010100

**Subsection - Assembler Syntax:**
EE.VCMP.GT.S32 qa, qx, qy

**Subsection - Description:**
This instruction compares 32-bit vector data. It compares the numerical values of the four 32-bit data segments in registers qx and qy. If the former is larger than the latter, it writes 0xFFFFFFF into the corresponding 32-bit data segment in register qa. Otherwise, it writes 0 to the segment.

**Subsection - Operation:**
```
qa[ 31: 0 ] = (qx[ 31: 0]>qy[ 31: 0 ]) ? 0xFFFFFFFF : 0
qa[ 63: 32 ] = (qx[ 63: 32]>qy[ 63: 32 ]) ? 0xFFFFFFFF : 0
...
qa[127:96] = (qx[127:96]>qy[127:96]) ? 0xFFFFFFFF : 0
```

**Footer Information:**
Espressif Systems  
ESP32-S3 TRM (Version 1.7)