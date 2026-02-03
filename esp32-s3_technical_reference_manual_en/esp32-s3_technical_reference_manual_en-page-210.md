**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.134 EE.VMULAS.S16.ACCX

**Instruction Word Table:**
- Instruction Word: `000110100`
- qy[2]: `0`
- qy[1:0]: `0`
- qx[2:0]: `10000100`

**Assembler Syntax Section:**
- Title: Assembler Syntax
- Content: EE.VMULAS.S16.ACCX qx, qy

**Description Section:**
- Description:
  This instruction divides registers qx and qy into 8 data segments by 16 bits. Then, it performs a signed multiply-accumulate operation on the 8 sets of segments respectively. The accumulated result is added to the value in special register ACCX. Then, the sum obtained is saturated and then stored in ACCX.

**Operation Section:**
- Title: Operation
- Content:
```
add0[31:0] = qx[ 15: 0] * qy[ 15: 0]
add1[31:0] = qx[ 31: 16] * qy[ 31: 16]
...
add7[31:0] = qx[127:112] * qy[127:112]
sum[40:0] = ACCX[39:0] + ad[31:0)d0[31:0] + ad[31:0)d1[31:0] + ... + ad[31:0)d7[31:0]
ACCX[39:0] = min(max(sum[40:0], -2^{39}), 2^{39}-1)
```

**Footer Information:**
- Espressif Systems
- Page Number and Document Version:
  ESP32-S3 TRM (Version 1.7)