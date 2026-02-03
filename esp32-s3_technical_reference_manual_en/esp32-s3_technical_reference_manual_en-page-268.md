**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.186 EE.VSL.32

**Subsection Titles and Content:**

- **Instruction Word:** 
  - `11 qs[2:1] 1101 qs[0] 01111110 qa[2:0] 0100`

- **Assembler Syntax**
  - EE.VSL.32 qa, qs

- **Description**
  - This instruction performs a left shift on the four 32-bit data segments in register qs respectively. The left shift amount is the value in the 6-bit special register SAR. During the shift process, the lower bits are padded with O. The lower 32 bits of the shift result are stored in the corresponding data segment in register qa.

- **Operation**
  - `qa[31: 0] = (qs[31: 0] << SAR[5:0])`
  - `qa[63: 32] = (qs[63: 32] << SAR[5:0])`
  - `qa[95: 64] = (qs[95: 64] << SAR[5:0])`
  - `qa[127: 96] = (qs[127: 96] << SAR[5:0])`

**Footer Information:**
- Espressif Systems
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback