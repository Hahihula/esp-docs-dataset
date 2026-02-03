**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.196 EE.VST.L.64.IP

**Subsection - Instruction Word Table:**
- Column Headers:
  1. imm8[7]
  2. qv[2:1]
  3. O100
  4. qv[0]
  5. imm8[6:0]
  6. as[3:0]
  7. O100

**Subsection - Assembler Syntax:**
EE.VST.L.64.IP qv, as, -1024..1016

**Subsection - Description:**
This instruction forces the lower 3 bits of the access address in register as to zero and stores the lower 64 bits in register qv to memory. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 3.

**Subsection - Operation:**
1. `qv[ 63: 0 ] => stored64({as[31:3],3{0}})`
2. `as[31:0] = as[31:0] + {21{imm8[7]},imm8[7:0],3{0}}`

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Link Texts:
  - Submit Documentation Feedback