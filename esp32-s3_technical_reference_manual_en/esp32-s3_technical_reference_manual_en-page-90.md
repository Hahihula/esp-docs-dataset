**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.14 EE.FFT.R2BF.S16.ST.INCP

**Instruction Word Table:**
- Instruction Word:
  - 11010000 sar[4:0] qy[2:0] 1 qao[2:0] qx[1:0] O sar[4:1] 0100 as[3:0] 111 qx[2]
- Description:
  - EE.FFT.R2BF.S16.ST.INCP qao0, qx, qy, as, 0..3

**Subsection Header:**
Assembler Syntax

**Description Text:**
This instruction performs the radix-2 butterfly operation on the 16-byte values in registers qx and qy, and the data bit width is 16 bits. Some of the calculation results are written to register qao0, and others implement an arithmetic shift and are written into the memory address indicated by as. After the access is completed, the value in register as is incremented by 16.

**Subsection Header:**
Operation

**Code Block (Markdown format):**
```
qao[ 15: 0] = qx[ 15: 0] - qy[ 15: 0]
qao[31: 16] = qx[31: 16] - qy[31: 16]
qao[47: 32] = qx[47: 32] - qy[47: 32]
qao[63: 48] = qx[63: 48] - qy[63: 48]
qao[79: 64] = qx[79: 64] - qy[79: 64]
qao[95: 80] = qx[95: 80] - qy[95: 80]
qao[111: 96] = qx[111: 96] - qy[111: 96]
qao[127:112] = qx[127:112] - qy[127:112]

{
    (qx[127:112] + qy[127:112]) >> sar4,
    (qx[111: 96] + qy[111: 96]) >> sar4,
    (qx[ 95: 80] + qy[ 95: 80]) >> sar4,
    (qx[ 79: 64] + qy[ 79: 64]) >> sar4,
    (qx[ 63: 48] + qy[ 63: 48]) >> sar4,
    (qx[ 47: 32] + qy[ 47: 32]) >> sar4,
    (qx[ 31: 16] + qy[ 31: 16]) >> sar4,
    (qx[ 15: 0] + qy[ 15: 0]) >> sar4
} => store128({as[31:4],4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Page Number: 90

**Link Texts:**
- GoBack
- Submit Documentation Feedback