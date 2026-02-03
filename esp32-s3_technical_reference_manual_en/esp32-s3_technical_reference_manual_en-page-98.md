**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.22 EE.LD.QACC_L.H.32.IP

**Subsection - Instruction Word:**
- 0 imm4[7] O101100 imm4[6:0] as[3:0] 0100

**Subsection - Assembler Syntax:**
EE.LD.QACC_L.H.32.IP as, -512..508

**Subsection - Description:**
This instruction forces the lower 2 bits of the access address in register `as` to zero and loads 32-bit data from memory to the special register QACC_L[159:128]. After the access is completed, the value in register `as` is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 2.

**Subsection - Operation (with code block):**
```
1. QACC_L[159:128] = lod32({as[31:2],2{0}})
2. as[31:0] = as[31:0] + {22 imm4[7]},imm4[7:0],2{0}}
```

**Footer Information:**
- Espressif Systems
- ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback