**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.75 EE.VADDS.S32.ST.INCP

**Instruction Word Table:**
- Instruction Word:
  - `1100100`
  - `qy[0]`
  - `qv[2:0]`
  - `1`
  - `qa[2:0]`
  - `qx[1:0]`
  - `qy[2:1]`
  - `0001`
  - `as[3:0]`
  - `111`
  - `qx[2]`

**Assembler Syntax Section:**
- **Title:** Assembler Syntax
- **Syntax Example:** EE.VADDS.S32.ST.INCP qv, as, qa, qx, qy

**Description Section:**
- This instruction performs a vector addition on 32-bit data in the two registers qx and qy. Then, the 4 results obtained from the calculation are saturated, and the saturated results are written to register qa.
- During the operation, the instruction forces the lower 4 bits of the access address in register as to 0 and stores the value in register qv to memory. After the access, the value in register as is incremented by 16.

**Operation Section:**
- **Title:** Operation
- **Operations Listed (with syntax examples):**
  - `qa[31: 0] = min(max(qx[31: 0] + qy[31: 0], -2^{31}-1)`
  - `qa[63: 32] = min(max(qx[63: 32] + qy[63: 32], -2^{31}-1)`
- **Additional Operations Listed (with syntax examples):**
  - `qv[127:0] => store128({as[31:4],4{0}})`
  - `as[31:0] = as[31:0] + 16`

**Footer Information:**
- "Espressif Systems"
- Page number and document version information:
  - "ESP32-S3 TRM (Version 1.7)"
- Link for submitting documentation feedback.

**Navigation Links:**
- GoBack

(Note: The text in the image is structured as described above, including section headers, tables, lists of operations with syntax examples.)