**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.199 EE.VSUBS.S16.LD.INCP

**Instruction Word Table:**
- qu[2:1] | qy[0]
- 100   | 110
- qu[0] | qa[2:0]
-      | qx[1:0]
-      | qy[2:1]
- as[3:0]| 111
-      | qx[2]

**Assembler Syntax:**
EE.VSUBS.S16.LD.INCP qu, as, qx, qy

**Description:**
This instruction performs a vector subtraction on 16-bit data. Registers qx and qy are the subtrahend and the minuend respectively. Then, the 8 results obtained from the calculation are saturated and then written into register qa.

During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access, the value in register as is incremented by 16.

**Operation:**
```
qa[ 15: 0] = min(max(qx[ 15: 0] - qy[ 15: 0], -2^15), 2^15-1)
qa[31: 16] = min(max(qx[31: 16] - qy[31: 16], -2^15), 2^15-1)
...
qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
Espressif Systems  
Page number: 282  
Document version and title: ESP32-S3 TRM (Version 1.7)