**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.71 EE.VADDS.S16.LD.INCP

**Subsection Headers and Content:**

- **Instruction Word**: 
  - `111000`
  - `qu[2:1]`: `qy[0]` or `O10`
  - `qu[0]`: `qa[2:0]` or `qa[1:0]`
  - `qa[2:0]`: `qy[2:1]` or `1101`
  - `as[3:0]`: `111`
  - `qx[2]`

- **Assembler Syntax**:
  - `EE.VADDS.S16.LD.INCP qu, as, qae, qx, qy`

- **Description**: 
  This instruction performs a vector addition on 16-bit data in the two registers qx and qy. Then, the 8 results obtained from the calculation are saturated, and the saturated results are written to register qa.
  
  During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access, the value in register as is incremented by 16.

- **Operation**:
  - `qa[ 15: 0] = min(max(qx[ 15: 0] + qy[ 15: 0], -2^{15}), 2^{15}-1)`
  - `qa[31: 16] = min(max(qx[31: 16] + qy[31: 16], -2^{15}), 2^{15}-1)`

- **Code Example**:
  ```
  qu[127:0] = load128({as[31:4],4{0}})
  as[31:0] = as[31:0] + 16
  ```

**Footer Information**: 
Espressif Systems  
Page number and document version:
ESP32-S3 TRM (Version 1.7)