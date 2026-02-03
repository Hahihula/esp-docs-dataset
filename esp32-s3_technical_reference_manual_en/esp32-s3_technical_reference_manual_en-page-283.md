**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.200 EE.VSUBS.S16.ST.INCP

**Instruction Word Table:**
| qy[0] | qv[2:0] | qa[2:0] | qx[1:0] | qy[2:1] | 0001 | as[3:0] | 111 | qx[2] |
|-------|---------|---------|---------|---------|------|--------|-----|-------|
|       |         |         |         |         |      |        |     |       |

**Assembler Syntax Section:**
- **Title:** Assembler Syntax
- **Syntax Example:** EE.VSUBS.S16.ST.INCP qv, as, qa, qx, qy

**Description Section:**
This instruction performs a vector subtraction on 16-bit data. Registers qx and qy are the subtrahend and the minuend respectively. Then, the 8 results obtained from the calculation are saturated and then written into register qa.

During the operation, the instruction forces the lower 4 bits of the access address in register as to 0 and stores the value in register qv to memory. After the access, the value in register as is incremented by 16.

**Operation Section:**
- **Title:** Operation
- **Code Example:**
```
qa[ 15: 0] = min(max(qx[ 15: 0] - qy[ 15: 0], -2^{15}), 2^{15}-1)
qa[31: 16] = min(max(qx[31: 16] - qy[31: 16], -2^{15}), 2^{15}-1)

qv[127:0] => store128({as[31:4],4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
- **Company:** Espressif Systems
- **Document Version and Type:** ESP32-S3 TRM (Version 1.7)
- **Page Number:** 283

**Navigation Links:**
- GoBack