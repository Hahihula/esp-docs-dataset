**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.74 EE.VADDS.S32.LD.INCP

**Subsection Titles and Content:**

- **Instruction Word:** 
  - 111000 | qu[2:1] | qy[0] | O11 | qu[0] | qa[2:0] | qx[1:0] | qy[2:1] | 1101 | as[3:0] | 111 | qx[2]

- **Assembler Syntax:** 
  - EE.VADDS.S32.LD.INCP qu, as, qqa, qx, qy

- **Description**
  - This instruction performs a vector addition on 32-bit data in the two registers qx and qy. Then, the 4 results obtained from the calculation are saturated, and the saturated results are written to register qa.
  - During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access, the value in register as is incremented by 16.

- **Operation**
  ```assembly
  qa[31:0] = min(max(qx[31:0] + qy[31:0], -2^{31}), 2^{31}-1)
  qa[63:32] = min(max(qx[63:32] + qy[63:32], -2^{31}), 2^{31}-1)
  ...
  
  qu[127:0] = load128({as[31:4],4{0}})
  as[31:0] = as[31:0] + 16
  ```

**Footer Information:** 
- Espressif Systems, ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback