**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
18.35 EE.LDQA.U8.128.IP

**Subsection Titles and Content:**

- **Instruction Word:** 
  - `0 imm16[7] 01010 imm16[6:0] as[3:0] 0100`

- **Assembler Syntax**
  - EE.LDQA.U8.128.IP as, -2048..2032

- **Description**
  - This instruction forces the lower 4 bits of the access address in register as to zero, loads 16-byte data from memory, divides it into 16 segments of 8 bits, zero-extends each segment to 20 bits, and then stores the results to the 160-bit special registers QACC_L and QACC_H respectively. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 4.

- **Operation**
  - `dataIn[127:0] = load128({as[31:4],4{0}})`
  - `QACC_L[19:0] = {12{0}, dataIn[7:0]}`
  - `QACC_L[39:20] = {12{0}, dataIn[15:8]}`
  - `QACC_L[59:40] = {12{0}, dataIn[23:16]}`
  - ...
  - `QACC_L[159:140] = {12{0}, dataIn[63:56]}`
  - `QACC_H[19:0] = {12{0}, dataIn[71:64]}`
  - `QACC_H[39:20] = {12{0}, dataIn[79:72]}`
  - `QACC_H[59:40] = {12{0}, dataIn[87:80]}`
  - ...
  - `QACC_H[159:140] = {12{0}, dataIn[127:120]}`
  - `as[31:0] = as[31:0] + {20{imm16[7]}, imm16[7:0], 4{0}}`

**Footer Information:**
- Espressif Systems
- Page number and document version information (111 ESP32-S3 TRM (Version 1.7))
- Link to submit documentation feedback