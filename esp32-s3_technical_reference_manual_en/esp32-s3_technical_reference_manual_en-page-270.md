**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PEX)

**Section Header:**
1.8.188 EE.VSMULAS.S16.QACC.LD.INCP

**Instruction Word Table:**
- qu[2:1] | qy[0] | qu[0] | sel8[2:0] | qx[1:0] | qy[2:1] | as[3:0] | qx[2]
  - 11000
  - 111

**Assembler Syntax:**
EE.VSMULAS.S16.QACC.LD.INCP qu, as, qx, qy, sel8

**Description:**
This instruction selects one out of the eight 16-bit data segments in register qy according to immediate number se18 and performs a signed multiplication on it and the eight 16-bit data segments in register qx respectively. The 8 results obtained are added to the corresponding 40-bit data segment in special registers QACC_H and QACC_L respectively, then the result is saturated to a 40-bit signed number and stored to the corresponding 40-bit data segment in QACC_H and QACC_L.

During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from memory to register qu. After the access, the value in register as is incremented by 16.

**Operation:**
```
temp[15:0] = qy[se18*16+15:sel8*16]
QACC_L[39:0] = min(max(QACC_L[39:0] + qx[15:0]: 0) * temp[15:0], -2^39), 2^39-1)
QACC_L[79:40] = min(max(QACC_L[79:40] + qx[31:16] * temp[15:0], -2^39), 2^39-1)
QACC_L[119:80] = min(max(QACC_L[119:80] + qx[47:32] * temp[15:0], -2^39), 2^39-1)
QACC_L[159:120] = min(max(QACC_L[159:120] + qx[63:48] * temp[15:0], -2^39), 2^39-1)
QACC_H[39:0] = min(max(QACC_H[39:0] + qx[79:64] * temp[15:0], -2^39), 2^39-1)
QACC_H[79:40] = min(max(QACC_H[79:40] + qx[95:80] * temp[15:0], -2^39), 2^39-1)
QACC_H[119:80] = min(max(QACC_H[119:80] + qx[111:96] * temp[15:0], -2^39), 2^39-1)
QACC_H[159:120] = min(max(QACC_H[159:120] + qx[127:112] * temp[15:0], -2^39), 2^39-1)

qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
Espressif Systems  
Page Number: 270  
Document Title: ESP32-S3 TRM (Version 1.7)  
Link Texts:
- Submit Documentation Feedback