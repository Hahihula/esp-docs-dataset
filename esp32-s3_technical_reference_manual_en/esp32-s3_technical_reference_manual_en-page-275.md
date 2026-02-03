**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.192 EE.VST.128.IP

**Subsection - Instruction Word Table:**
- Column headers:
  - `imm16[7]`
  - `qv[2:1]`
  - `1010`
  - `qv[0]`
  - `imm16[6:0]`
  - `as[3:0]`
  - `0100`

**Subsection - Assembler Syntax:**
- Text:
  EE.VST.128.IP qv, as, -2048..2032

**Subsection - Description:**
This instruction forces the lower 4 bits of the access address in register as to zero and stores the 128 bits in register qv to memory. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Subsection - Operation:**
- Text:
  ```
  1   qv[127:0] => store128({as[31:4],4{0}})
  2   as[31:0] = as[31:0] + {20{imm16[7]},imm16[7:0],4{0}}
  ```

**Footer Information:**
- Left-aligned text:
  - "Espressif Systems"
  - Page number and document version information (centered): `275 ESP32-S3 TRM (Version 1.7)`
- Right-aligned link-texts:
  - "Submit Documentation Feedback"