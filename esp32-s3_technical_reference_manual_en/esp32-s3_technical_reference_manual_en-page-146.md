**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.70 EE.VADDS.S16

**Instruction Word Breakdown Table:**
- `10`
- `qa[2:1]`: `1110`
- `qa[0]`: `0`
- `qy[2]`: `0`
- `qy[1:0]`: `0x10`
- `qy[2:0]`: `0x0100`

**Subsection Title:**
Assembler Syntax

**Syntax Description:**
EE.VADDS.S16 qa, qx, qy

**Description Section:**
This instruction performs a vector addition on 16-bit data in the two registers qx and qy. Then, the 8 results obtained from the calculation are saturated, and the saturated results are written to register qa.

**Operation Section (with code examples):**
```
qa[ 15: 0 ] = min(max(qx[ 15: 0 ] + qy[ 15: 0 ], -2^15), 2^15)-1
qa[ 31: 16 ] = min(max(qx[ 31: 16 ] + qy[ 31: 16 ], -2^15), 2^15)-1

...
```

**Footer Information:**
Espressif Systems  
Page number and document version information at the bottom of the page.