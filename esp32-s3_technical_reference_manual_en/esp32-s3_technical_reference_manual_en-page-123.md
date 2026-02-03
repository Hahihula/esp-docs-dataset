**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.47 EE.SLCI.2Q

**Subsection - Instruction Word Table:**
- `11`: `qs1[2:1]`
- `100`: `qs1[0]`
- `0`: `qs0[2:0]`
- `0110`: `sar16[3:0]`
- `0100`: (Blank)

**Subsection - Assembler Syntax:**
EE.SLCI.2Q qs1, qs0, 0..15

**Subsection - Description:**
This instruction performs a left shift on the 32-byte concatenation of registers qs0 and qs1 and pads the lower bits with 0. The upper 128 bits of the shift result is written to register qs1 and the lower 128 bits is written to qs0. The left shift amount is 8 times the sum of sar16 and 1.

**Subsection - Operation:**
```
{qs1[127: 0], qs0[127: 0]} = {qs1[127: 0], qs0[127: 0]} << ((sar16[3:0]+1)*8)
``` 

**Footer Information:**
Espressif Systems
Page number: 123
Document version and title: ESP32-S3 TRM (Version 1.7)

**Link Texts:**
- GoBack

**Action Links at the Bottom of Page:**
Submit Documentation Feedback