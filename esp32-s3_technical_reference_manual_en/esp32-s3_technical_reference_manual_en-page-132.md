**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.56 EE.SRCQ.128.ST.INCP

**Subsection - Instruction Word Table:**
- `11`: qs1[2:1]
- `1100`: qs0
- `1100`: qs0[2:0]
- `1110`: as[3:0]
- `0100`

**Subsection - Assembler Syntax:**
EE.SRCQ.128.ST.INCP qs0, qs1, as

**Subsection - Description:**
This instruction performs an arithmetic right shift on the 32-byte concatenation of registers qs0 and qs1.
Then, it writes the lower 128 bits of the shift result to memory. After the access, the value in register as is incremented by 16.

**Subsection - Operation (with code snippet):**
```
{qs1[127: 0], qs0[127: 0]} >> {SAR_BYTE[3:0] << 3} => store128({as[31:4],4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback

**Document Version and Page Number:**
ESP32-S3 TRM (Version 1.7)  
Page number not specified in the provided text, but it is indicated at page end as "132".