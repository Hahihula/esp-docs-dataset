**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.121 EE.VMIN.S8.ST.INCP

**Instruction Word Table:**
- Instruction Word:
  - 1100101 | qy[0] | qv[2:0] | O | qa[2:0] | qx[1:0] | qy[2:1] | 0010 | as[3:0] | 111 | qx[2]

**Assembler Syntax Section:**
- Title: Assembler Syntax
- Content:
  - EE.VMIN.S8.ST.INCP qv, as, qa, qx, qy

**Description Section:**
- Description Text:
  - This instruction compares numerical values of the 16-bit vector data segments in registers qx and qy. The data segment with the smaller value is written into the corresponding 8-bit data segment in register qa.
  - During the operation, the instruction forces the lower 4 bits of the access address in register as to 0 and stores the value in register qv to memory. After the access, the value in register as incremented by 16.

**Operation Section:**
- Operation Text:
  ```
  qa[7: 0] = (qx[7: 0] <=qy[7: 0]) ? qx[7: 0] : qy[7: 0]
  qa[15: 8] = (qx[15: 8] <=qy[15: 8]) ? qx[15: 8] : qy[15: 8]
  ...
  qa[127:120] = (qx[127:120] <=qy[127:120]) ? qx[127:120] : qy[127:120]

  qv[127:0] => store128({as[31:4],4{0}})
  as[31:0] = as[31:0] + 16
  ```

**Footer Information:**
- Company Name:
  - Espressif Systems

- Document Version and Link:
  - ESP32-S3 TRM (Version 1.7)
  - Submit Documentation Feedback