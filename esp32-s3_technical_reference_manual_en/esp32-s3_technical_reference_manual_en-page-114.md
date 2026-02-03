**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.38 EE.MOV.S16.QACC

**Subheading - Instruction Word:**
- 11 qs[2:1] 1101 qs[0] 111111100100100

**Subheading - Assembler Syntax:**
EE.MOV.S16.QACC qs

**Subheading - Description:**
This instruction sign-extends the 8 segments of 16-bit data in register qs to 40 bits and writes the result to the special registers QACC_H and QACC_L.

**Subheading - Operation Table (with code):**

```
QACC_L[39: 0] = {24{qs[15]}, qs[ 15: 0]}
QACC_L[79: 40] = {24{qs[31]}, qs[ 31: 16]}
QACC_L[119:80] = {24{qs[47]}, qs[ 47: 32]}
QACC_L[159:120] = {24{qs[63]}, qs[ 63: 48]}

QACC_H[39: 0] = {24{qs[79]}, qs[ 79: 64]}
QACC_H[79: 40] = {24{qs[95]}, qs[ 95: 80]}
QACC_H[119:80] = {24{qs[95]}, qs[111: 96]}
QACC_H[159:120] = {24{qs[95]}, qs[127:112]}
```

**Footer Information:**
- Page number and document version information:
  - "Espressif Systems"
  - "ESP32-S3 TRM (Version 1.7)"
  - "Submit Documentation Feedback"