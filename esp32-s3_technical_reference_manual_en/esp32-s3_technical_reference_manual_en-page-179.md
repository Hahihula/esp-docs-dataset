**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.103 EE.VLDHBC.16.INCP

**Subsection Titles and Content:**

- **Instruction Word:** 
  - `qu[2:1]`: 11
  - `qu[0]`: 1100
  - `qu1[2:0]`: 0010
  - `as[3:0]`: as[3:0]
  - `0100`

- **Assembler Syntax:** 
  - EE.VLDHBC.16.INCP qu, qu1, as

- **Description:**
  This instruction forces the lower 4 bits of the access address in register as to zero, loads 16-byte data from memory, extends it to 256 bits according to the following way, and assigns the result to registers qu and qu1. After the access, the value in register as is incremented by 16.

- **Operation:**
  ```plaintext
  dataIn[127:0] = load128(as[31:4], 4{0})
  
  qu = {2[dataIn[63: 48]], 2[dataIn[ 47: 32]], 2[dataIn[ 31: 16]], 2[dataIn[ 15:
      0]]}
  
  qu1 = {2[dataIn[127:112]], 2[dataIn[111: 96]], 2[dataIn[ 95: 80]], 2[dataIn[ 79:
      64]]}
  
  as[31:0] = as[31:0] + 16
  ``` 

**Footer Information:** 
- Espressif Systems, ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback