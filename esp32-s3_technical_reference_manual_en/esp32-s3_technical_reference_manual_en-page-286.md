**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.203 EE.VSUBS.S32.ST.INCP

**Subsection - Instruction Word Table:**
- Instruction Word:
  - `1101000`
  - `qy[0]`
  - `qv[2:0]`
  - `1`
  - `qa[2:0]`
  - `qx[1:0]`
  - `qy[2:1]`
  - `0010`
  - `as[3:0]`
  - `111`
  - `qx[2]`

**Subsection Title:**
Assembler Syntax

**Body Text:**
EE.VSUBS.S32.ST.INCP qv, as, qa, qx, qy

**Description Section:**
This instruction performs a vector subtraction on 32-bit data. Registers qx and qy are the subtrahend and the minuend respectively. Then, the 4 results obtained from the calculation are saturated and then written into register qa.

During the operation, the instruction forces the lower 4 bits of the access address in register as to 0 and stores the value in register qv to memory. After the access, the value in register as is incremented by 16.

**Operation Section:**
```plaintext
qa[31: 0] = min(max(qx[31: 0] - qy[31: 0], -2^{31}), 2^{31}-1)
qa[63: 32] = min(max(qx[63: 32] - qy[63: 32], -2^{31}), 2^{31}-1)

qv[127:0] => store128({as[31:4],4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
Espressif Systems  
Page number: 286  
Document version and title: ESP32-S3 TRM (Version 1.7)