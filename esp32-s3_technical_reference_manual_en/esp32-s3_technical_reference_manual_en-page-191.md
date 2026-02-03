**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.115 EE.VMIN.S16.ST.INCP

**Instruction Word Table:**
- qy[0]
- qv[2:0]
- O
- qa[2:0]
- qx[1:0]
- qy[2:1]
- 0001
- as[3:0]
- 111
- qx[2]

**Assembler Syntax Section:**
EE.VMIN.S16.ST.INCP qv, as, qa, qx, qy

**Description Section:**
This instruction compares numerical values of the eight 16-bit vector data segments in registers qx and qy. The data segment with the smaller value is written into the corresponding 16-bit data segment in register qx.

During the operation, the instruction forces the lower 4 bits of the access address in register as to 0 and stores the value in register qv to memory. After the access, the value in register as is incremented by 16.

**Operation Section:**
```
qa[ 15: 0 ] = (qx[ 15: 0 ]<=qy[ 15: 0 ]) ? qx[ 15: 0 ] : qy[ 15: 0 ]
qa[ 31: 16 ] = (qx[ 31: 16]<=qy[ 31: 16 ]) ? qx[ 31: 16 ] : qy[ 31: 16 ]

...
qa[127:112] = (qx[127:112]<=qy[127:112]) ? qx[127:112] : qy[127:112]

qv[127:0] => store128({as[31:4],4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
Espressif Systems  
Page Number: 191  
Document Title: ESP32-S3 TRM (Version 1.7)  
Link Texts:
- Submit Documentation Feedback