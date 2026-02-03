**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.64 EE.ST.UA_STATE.IP

**Subsection - Instruction Word:**
- 0 imm[7] 0111000 imm[6:0] as[3:0] 0100

**Subsection - Assembler Syntax:**
EE.ST.UA_STATE.IP as, -2048..2032

**Subsection - Description:**
This instruction forces the lower 4 bits of the access address in register as to zero and stores the 128 bits data in special register UA_STATE to memory. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Subsection - Operation:**
```
UA_STATE[127:0] => store128({as[31:4],4{0}})
as[31:0] = as[31:0] + {20{imm16[7]},imm16[7:0],4{0}}
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback