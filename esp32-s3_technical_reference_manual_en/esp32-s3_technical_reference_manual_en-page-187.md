**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.111 EE.VMAX.S8.LD.INCP

**Instruction Word Table:**
- qu[2:1]: qy[0]
- qu[0]: 001
- qa[2:0]: qu[0]
- qx[1:0]: 1111
- qx[2:1]: as[3:0]
- qx[2]: 111

**Assembler Syntax:**
EE.VMAX.S8.LD.INCP qy, as, qa, qx, qy

**Description:**
This instruction compares numerical values of the 16-bit vector data segments in registers qx and qy. The data segment with the larger value is written into the corresponding 8-bit data segment in register qa.

During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access, the value in register as is incremented by 16.

**Operation:**
```
qa[7:0] = (qx[7:0]>qy[7:0]) ? qx[7:0] : qy[7:0]
qa[15:8] = (qx[15:8]>qy[15:8]) ? qx[15:8] : qy[15:8]
...
qa[127:120] = (qx[127:120]>qy[127:120]) ? qx[127:120] : qy[127:120]

qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
Espressif Systems  
Page number: 187  
Document version and title: ESP32-S3 TRM (Version 1.7)