**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
18.12 EE.FFT.CMUL.S16.ST.XP

**Instruction Word Table:**
- sar4[1:0]
- upd4[1:]
- sel8[0]
- qy[2:0]
- upd4[0]
- qxv[2:0]
- qx[1:0]
- sel8[2:1]
- ad[3:0]
- as[3:0]
- 111
- qx[2]

**Assembler Syntax:**
EE.FFT.CMUL.S16.ST.XP qx, qy, qv, as, ad, sel8, upd4, sar4

**Description:**
This instruction performs a 16-bit signed complex multiplication. It is similar to EE.CMUL.S16 except that the order of registers qx and qy is reversed.

The result of the operation and the data segments in registers qx and qv specified by the immediate data upd4 are concatenated into 128 bits, which then are written into memory. After the access is completed, the value in register as is incremented by the value in register ad.

**Operation:**
- if sel8 == 6:
  - temp[15:0] = (qx[111:96] * qy[111:96] + qxv[127:112] * qy[127:112]) >> SAR[5:0]
- if sel8 == 7:
  - temp[15:0] = (qx[111:96] * qy[111:96] - qxv[127:112] * qy[127:112]) >> SAR[5:0]
- if sel8 == 8:
  - temp[15:0] = (qx[111:96] * qy[111:96] + qxv[127:112] * qy[127:112]) >> SAR[5:0]

**Code Block 1:**
```assembly
if upd4 == 0:
  {temp[31:0], qv[95:0]} => store128({as[31:4],4{0}})
if upd4 == 1 // radix2 last second stage
{
  temp[31:0],
  qx[95:64],
  qx[63:48] >> sar4,
  qx[47:32] >> sar4,
  qx[31:16] >> sar4,
  qx[15:0] >> sar4
} => store128({as[31:4],4{0}})
if upd4 == 2 // radix2 last stage
{
  temp[31:0],
  qx[63:48] >> sar4,
  qx[47:32] >> sar4,
  qx[95:64],
  qx[31:16] >> sar4,
  qx[15:0] >> sar4
} => store128({as[31:4],4{0}})
```

**Code Block 2:**
```assembly
if upd4 == 2 // radix2 last stage
{
  temp[31:0],
  qx[63:48] >> sar4,
  qx[47:32] >> sar4,
  qx[95:64],
  qx[31:16] >> sar4,
  qx[15:0] >> sar4
} => store128({as[31:4],4{0}})
```

**Footer Information:**
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback