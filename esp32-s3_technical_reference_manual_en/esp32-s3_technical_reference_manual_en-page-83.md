**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
18.7 EE.FFT.AMS.S16.LD.INCP

**Instruction Word Table:**
- 110100
- sel2[0]
- qz1[2]
- qz0[]
- qy[2:0]
- qz1[1]
- qm[2:0]
- qx[1:0]
- qx[2:1]
- qx1[0]
- qu[2:0]
- as[3:0]

**Subsection Title:**
Assembler Syntax

**Subsection Content:**
EE.FFT.AMS.S16.LD.INCP qqu, as, qz, qz1, qx, qy, qm, sel2

**Description Section:**
It is a dedicated FFT instruction to perform addition, subtraction, multiplication, addition and subtraction, and shift operations on 16-bit data segments.

During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access, the value in register as is incremented by 16.

**Operation Section:**
- temp0[15:0] = qx[47:32] + qy[47:32]
- temp1[15:0] = qx[63:48] - qy[63:48]

if sel2==0:
  temp2[15:0] = ((qx[47:32] - qy[47:32]) * qx[47:32] - (qx[63:48] + qy[48]) * qx[63:48]) >> SAR
  temp3[15:0] = ((qx[47:32] - qy[47:32]) * qx[63:48] + (qx[63:48] + qx[47:32]) * qx[63:48])
  temp2[15:0] = ((qx[63:48] - qx[47:32]) >> SAR

if sel2==1:
  temp2[15:0] = ((qx[63:48] + qx[47:32]) * qx[63:48])
  temp3[15:0] = ((qx[63:48] - qx[47:32]) >> SAR)
  temp2[15:0] = ((qx[63:48] + qx[47:32]) * qx[63:48])

qz[47:32] = temp0[15:0] + temp2[15:0]
qz[63:48] = temp1[15:0] + temp3[15:0]
qz1[47:32] = temp0[15:0] - temp2[15:0]
qz1[63:48] = temp3[15:0] - temp1[15:0]

qu = load128({as[31:4],4,0})
as[31:0] = as[31:0] + 16

**Footer Information:**
Espressif Systems
Page Number: 83
Document Title: ESP32-S3 TRM (Version 1.7)
Link Texts:
- GoBack
- Submit Documentation Feedback