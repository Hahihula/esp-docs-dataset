**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.57 EE.SRCXXP.2Q

**Subsection Titles and Content:**

- **Instruction Word:** 
  - `11` `qs[2:1]` `0110` `qs[0]` `qs0[2:0]` `ad[3:0]` `as[3:0]` `0100`

- **Assembler Syntax**
  - `EE.SRCXXP.2Q qs1, qs0, as, ad`

- **Description**
  - This instruction performs a logical right shift on the 32-byte concatenation of registers qs0 and qs1 and pads the higher bits with O. The upper 128 bits of the shift result is written to register qs1 and the lower 128 bits is written to qs0. The right shift amount is 8 multiplied by the sum of 1 plus the lower 4-bit value of register as.
  - After these operations, the value in as is incremented by the value in ad.

- **Operation**
  ```
  {qs1[127: 0], qs0[127: 0]} = {qs1[127: 0], qs0[127: 0]} >> ((as[3:0]+1)*8)
  qs1[127:127-8*as[3: 0]] = 0
  as[31:0] = as[31:0] + ad[31:0]
  ``` 

**Footer Information:** 
- Espressif Systems
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback