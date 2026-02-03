**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.114 EE.VMIN.S16.LD.INCP

**Subsection Titles and Content:**

- **Instruction Word:** 
  - 111000 qu[2:1] qy[0] O10 qu[0] qa[2:0] qx[1:0] qy[2:1] as[3:0] 111 qx[2]

- **Assembler Syntax:** 
  - EE.VMIN.S16.LD.INCP qu, as, qa, qx, qy

- **Description**
  - This instruction compares numerical values of the eight 16-bit vector data segments in registers qx and qy. The data segment with the smaller value is written into the corresponding 16-bit data segment in register qa.
  - During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access, the value in register as is incremented by 16.

- **Operation**
  - ```
    qa[15: 0] = (qx[15: 0]<=qy[15: 0]) ? qx[15: 0] : qy[15: 0]
    qa[31: 16] = (qx[31: 16]<=qy[31: 16]) ? qx[31: 16] : qy[31: 16]
    ...
    qa[127:112] = (qx[127:112]<=qy[127:112]) ? qx[127:112] : qy[127:112]
    qu[127:0] = load128({as[31:4],4{0}})
    as[31:0] = as[31:0] + 16
  ```

**Footer Information:** 
- Espressif Systems, ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback