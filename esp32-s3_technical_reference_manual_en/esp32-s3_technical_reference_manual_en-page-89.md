**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.13 EE.FFT.R2BF.S16

**Instruction Word Table:**
- 11 | qa0[2:1] | 1100 | qa0[0] | qa1[2:0] | qy[2:1] | 0 | sel2[0] | qx[2:1] | qy[0] | qx[0] | 0100

**Assembler Syntax Section Title:**
Assembler Syntax

**Syntax Line Example:**
EE.FFT.R2BF.S16 qa0, qa1, qx, qy, sel2

**Description Subsection Header:**
Description

**Description Text:**
This instruction performs the radix-2 butterfly operation on the 16-byte values in registers qx and qy, and the data bit width is 16 bits. Some of the calculation results are written to register qa0, and others are written to register qy.

**Operation Subsection Header:**
Operation

**Code Block (with comments):**

```
if sel2==0:
    op_a[127: 0] = {qy[63: 0], qx[ 63: 0]}
    op_b[127: 0] = {qx[127: 64], qy[127: 64]}
if sel2==1:
    op_a[127: 0] = {qy[95: 64], qx[31: 0], qx[ 95: 64], qx[ 31: 0]}
    op_b[127: 0] = {qx[127: 96], qx[ 63: 32], qx[127: 96], qx[ 63: 32]}
    qa0[ 15: 0] = op_a[15: 0] + op_b[ 15: 0]
    qa0[ 31: 16] = op_a[31: 16] + op_b[ 31: 16]
    qa0[47: 32] = op_a[47: 32] + op_b[47: 32]
    qa0[63: 48] = op_a[63: 48] + op_b[63: 48]
    qa0[79: 64] = op_a[79: 15] - op_b[ 15: 0]
    qa0[95: 80] = op_a[31: 16] + op_b[31: 16]
    qa0[111: 96] = op_a[47: 32] - op_b[ 47: 32]
    qa0[127:112] = op_a[63: 48] + op_b[63: 48]

qa1[ 15: 0] = op_a[79: 64] + op_b[ 79: 64]
qa1[ 31: 16] = op_a[95: 80] + op_b[95: 80]
qa1[47: 32] = op_a[111: 96] + op_b[111: 96]
qa1[63: 48] = op_a[127:112] + op_b[127:112]
qa1[79: 64] = op_a[79: 64] - op_b[ 79: 64]
qa1[95: 80] = op_a[95: 80] + op_b[95: 80]
qa1[111: 96] = op_a[111: 96] - op_b[111: 96]

qa1[127:112] = op_a[127:112] - op_b[127:112]
```

**Footer Information:**
Espressif Systems
Page Number (89)
ESP32-S3 TRM (Version 1.7)

**Navigation Links at the Bottom of Page:** 
- Submit Documentation Feedback