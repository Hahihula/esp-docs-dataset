**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.194 EE.VST.H.64.IP

**Subsection - Instruction Word Table:**
- imm8[7]
- qv[2:1]
- 1011
- qv[0]
- imm8[6:0]
- as[3:0]
- o100

**Subsection Title:**
Assembler Syntax

**Body Text:**
EE.VST.H.64.IP qv, as, -1024..1016

**Subtitle: Description**

**Description Body Text:**
This instruction forces the lower 3 bits of the access address in register as to 0 and stores the upper 64 bits in register qv to memory. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 3.

**Subtitle: Operation**

**Operation Body Text with Code Blocks:**
1. `qv[127: 64] = stored64({as[31:3],3{0}})`
2. `as[31:0] = as[31:0] + {21{imm8[7]},imm8[7:0],3{0}}`

**Footer Information:**
Espressif Systems
Submit Documentation Feedback

**Document Version and Title:**
ESP32-S3 TRM (Version 1.7)