**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.123 EE.VMUL.S16.LD.INCP

**Instruction Word Table:**
- qu[2:1]: 011
- qy[0]: O11
- qu[0]: 
- qz[2:0]:
- qx[1:0]:
- qy[2:1]:
- as[3:0]:
- qx[2]:

**Assembler Syntax Table:**
EE.VMUL.S16.LD.INCP qu, as, qx, qx, qy

**Description Section:**
This instruction performs a signed vector multiplication on 16-bit data. Registers qx and qy are the multiplier and the multiplicand respectively. The eight 32-bit data results obtained from the calculation is arithmetically right-shifted by the value in special register SAR. Then, the lower 16-bit data of the shift result is written into corresponding segment of register qx.

During the operation, the lower 4 bits of the address access in register as are forced to be O, and then the 16-byte data is loaded from the memory to register qu. After the access, the value in register as is incremented by 16.

**Operation Section:**
```
qz[ 15: 0 ] = (qx[ 15: 0 ] * qy[ 15: 0 ]) >> SAR[5:0]
qz[ 31: 16 ] = (qx[ 31: 16 ] * qy[ 31: 16 ]) >> SAR[5:0]
qz[ 47: 32 ] = (qx[ 47: 32 ] * qy[ 47: 32 ]) >> SAR[5:0]
qz[ 63: 48 ] = (qx[ 63: 48 ] * qy[ 63: 48 ]) >> SAR[5:0]
qz[ 79: 64 ] = (qx[ 79: 64 ] * qy[ 79: 64 ]) >> SAR[5:0]
qz[ 95: 80 ] = (qx[ 95: 80 ] * qy[ 95: 80 ]) >> SAR[5:0]
qz[111: 96 ] = (qx[111: 96 ] * qy[111: 96 ]) >> SAR[5:0]
qz[127:112] = (qx[127:112] * qy[127:112]) >> SAR[5:0]

qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
Espressif Systems  
Page Number: 199  
Document Title: ESP32-S3 TRM (Version 1.7)  
Link Texts:
- Submit Documentation Feedback