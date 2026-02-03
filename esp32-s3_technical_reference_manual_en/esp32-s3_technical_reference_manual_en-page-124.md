**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.48 EE.SLCXXP.2Q

**Instruction Word Table:**
| 10 | qs1[2:1] | 0110 | qs1[0] | qs0[2:0] | ad[3:0] | as[3:0] | O100 |
|----|----------|------|--------|---------|--------|--------|------|
|    |          |      |        |         |        |        |      |

**Subheading - Assembler Syntax:**
EE.SLCXXP.2Q qs1, qs0, as, ad

**Description Section:**
This instruction performs a left shift on the 32-byte concatenation of registers qs0 and qs1 and pads the lower bits with 0. The upper 128 bits of the shift result is written to register qs1 and the lower 128 bits is written to qs0. The left shift amount is 8 multiplied by the sum of 1 plus the lower 4-bit value of register as. After the above operations, the value in qs is incremented by the value in ad.

**Operation Section:**
```
{qs1[127: 0], qs0[127: 0]} = {qs1[127: 0], qs0[127: 0]} << ((as[3:0]+1)*8)
as[31:0] = as[31:0] + ad[31:0]
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)

**Navigation Links:**
Submit Documentation Feedback

**GoBack Link:** 
GoBack