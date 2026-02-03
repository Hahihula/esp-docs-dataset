**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.109 EE.VMAX.S32.ST.INCP

**Instruction Word Table:**
- Instruction Word:
  - `11100101`
  - `qy[0]`
  - `qv[2:0]`
  - `O`
  - `qa[2:0]`
  - `qx[1:0]`
  - `qy[2:1]`
  - `0000`
  - `as[3:0]`
  - `111`
  - `qx[2]`

**Assembler Syntax Section:**
- **Title:** Assembler Syntax
- **Syntax:** EE.VMAX.S32.ST.INCP qy, as, qa, qx, qy

**Description Section:**
- This instruction compares numerical values of the four 32-bit vector data segments in registers qx and qy. The data segment with the larger value is written into the corresponding 32-bit data segment in register qa.
- During the operation, the instruction forces the lower 4 bits of the access address in register as to 0 and stores the value in register qv to memory. After the access, the value in register as is incremented by 16.

**Operation Section:**
- **Title:** Operation
- **Body Text with Code Blocks:**
  ```
  qa[31: 0] = (qx[31: 0]>>=qy[31: 0]) ? qx[31: 0] : qy[31: 0]
  qa[63: 32] = (qx[63: 32]>>=qy[63: 32])? qx[63: 32]: qy[63: 32]
  ...
  qa[127:96] = (qx[127:96]>>=qy[127:96]) ? qx[127:96] : qy[127:96]
  
  qv[127:0] => store128({as[31:4],4{0}})
  as[31:0] = as[31:0] + 16
  ```

**Footer Information:**
- Espressif Systems, ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback