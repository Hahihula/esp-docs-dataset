**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.78 EE.VADDS.S8.ST.INCP

**Instruction Word Table:**
- Instruction Word | qy[0] | qv[2:0] | qa[2:0] | qa[1:0] | qy[2:1] | 0010 | as[3:0] | 111 | qx[2]
- 11100100

**Assembler Syntax Section:**
- **Title:** Assembler Syntax
- **Syntax:** EE.VADDS.S8.ST.INCP qy, as, qa, qx, qy

**Description Section:**
- This instruction performs a vector addition on 8-bit data in the two registers qx and qy. Then, the 16 results obtained from the calculation are saturated, and the saturated results are written to register qa.
- During the operation, the instruction forces the lower 4 bits of the access address in register as to 0 and stores the value in register qv to memory. After the access, the value in register as is incremented by 16.

**Operation Section:**
- **Title:** Operation
- **Operations Listed (in pseudo-code):**
  - qa[7: 0] = min(max(qx[7: 0] + qy[7: 0], -2^{7}), 2^{7}-1)
  - qa [15: 8] = min(max(qx[15: 8] + qx[15: 8], -2^{7}), 2^{7}-1)
- **Additional Operations Listed (in pseudo-code):**
  - ...
  - qv[127:0] => store128({as[31:4],4{0}})
  - as[31:0] = as[31:0] + 16

**Footer Information:**
- Espressif Systems
- Page Number and Document Version (bottom center): ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback link