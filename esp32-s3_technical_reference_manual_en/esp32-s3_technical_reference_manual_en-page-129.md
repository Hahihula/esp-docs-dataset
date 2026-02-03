**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.53 EE.SRCI.2Q

**Subsection - Instruction Word Table:**
- 11 qs1[2:1] 1100 qs1[0] qs0[2:0] 1010 sar16[3:0] 0100

**Subsection Title:**
Assembler Syntax

**Body Text - Description:**
EE.SRCI.2Q qs1, qs0, sar16

This instruction performs a logical right shift on the 32-byte concatenation of registers qs0 and qs1 and pads the higher bits with O. The upper 128 bits of the shift result is written to register qs1 and the lower 128 bits is written to qs0. The right shift amount is 8 times the sum of sar16 and 1.

**Subsection Title:**
Operation

**Body Text - Operation Explanation (with code):**
```
{qs1[127: 0], qs0[127: 0]} = {qs1[127: 0], qs0[127: 8]}
qs1[127:127-8*sar16] = 0
```

**Footer Information:**
Espressif Systems  
ESP32-S3 TRM (Version 1.7)  

**Link Texts at the Bottom of Page:**
Submit Documentation Feedback