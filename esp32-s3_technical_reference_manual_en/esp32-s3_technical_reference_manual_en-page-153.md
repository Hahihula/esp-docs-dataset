**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.77 EE.VADDS.S8.LD.INCP

**Instruction Word Table:**
- qu[2:1]: 001
- qy[0]: 001
- qu[0]: 001
- qa[2:0]: 001
- qx[1:0]: 001
- qy[2:1]: 1100
- as[3:0]: 1100

**Assembler Syntax Table:**
- EE.VADDS.S8.LD.INCP qu, as, qa, qx, qy

**Description Section:**
This instruction performs a vector addition on 8-bit data in the two registers qx and qy. Then, the 16 results obtained from the calculation are saturated, and the saturated results are written to register qa.

During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access, the value in register as is incremented by 16.

**Operation Section:**
```plaintext
qa[7:0] = min(max(qx[7:0] + qy[7:0], -2^7), 2^7-1)
qa[15:8] = min(max(qx[15:8] + qy[15:8], -2^7), 2^7-1)

qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
Espressif Systems  
ESP32-S3 TRM (Version 1.7)