**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.158 EE.VMULAS.U16.ACCX

**Subsection - Instruction Word:**
000010100 | qy[2:0] | 0 | qy[1:0] | qx[2:0] | 10000100

**Subsection - Assembler Syntax:**
EE.VMULAS.U16.ACCX, qx, qy

**Subsection - Description:**
This instruction divides registers qx and qy into 8 data segments by 16 bits. Then, it performs an unsigned multiply-accumulate operation on the 8 sets of segments respectively. The accumulated result is added to the value in special register ACCX. Then, the sum obtained is saturated and then stored in ACCX.

**Subsection - Operation:**
```
add0[31:0] = qx[ 15: 0] * qy[ 15: 0]
add1[31:0] = qx[ 31: 16] * qy[ 15: 16]
...
add7[31:0] = qx[127:112] * qy[127:112]
sum[40:0] = ACCX[39:0] + ad[31:0)d0[31:0] + ad[31:0)d1[31:0] + ... + ad[31:0)d7[31:0]
ACCX[39:0] = min(max(sum[40:0], 0), 2^{40}-1)
```