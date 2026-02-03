**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.208 EE.VUNZIP.32

**Subsection Titles and Content:**

- **Instruction Word:** 
  - `11 qs1[2:1] 1100 qs0[0] qs0[2:0] 001110010100`

- **Assembler Syntax**
  - `EE.VUNZIP.32 qs0, qs1`

- **Description**
  - This instruction implements the unzip algorithm on 32-bit vector data.

- **Operation**:
  ```
  qs0[ 31: 0 ] = qs0[ 31: 0 ]
  qs0[ 63: 32 ] = qs0[ 95: 64 ]
  qs0[ 95: 64 ] = qs1[ 31: 0 ]
  qs0[127: 96 ] = qs1[ 95: 64 ]
  qs1[ 31: 0 ] = qs0[63: 32 ]
  qs1[ 63: 32 ] = qs0[127: 96 ]
  qs1[ 95: 64 ] = qs1[ 63: 32 ]
  qs1[127: 96 ] = qs1[127: 96 ]
  ```

**Footer Information:**
- Espressif Systems
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback