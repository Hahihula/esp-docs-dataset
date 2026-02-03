**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.41 EE.MOV.U8.QACC

**Subsection - Instruction Word:**
- **Instruction Word:** `11 qs[2:1] 1101 qs[0] 11111110110100`

**Subsection - Assembler Syntax:**
- **Assembler Syntax:** `EE.MOV.U8.QACC qs`

**Subsection - Description:**
- This instruction zero-extends the 16 segments of 8-bit data in register qs to 20 bits and writes the result to special registers QACC_H and QACC_L.

**Subsection - Operation (with code block):**

```
QACC_L[19: 0] = {12{0}, qs[ 7: 0]}
QACC_L[39: 20] = {12{0}, qs[ 15: 8]}
QACC_L[59: 40] = {12{0}, qs[ 23: 16]}
...
QACC_L[159:140] = {12{0}, qs[ 63: 56]}
QACC_H[ 19: 0]   = {12{0}, qs[ 71: 64]}
QACC_H[ 39: 20]  = {12{0}, qs[ 79: 72]}
QACC_H[ 59: 40]  = {12{0}, qs[ 87: 80]}
...
QACC_H[159:140] = {12{0}, qs[127:120]}
```

**Footer Information:**
- Espressif Systems
- Page number and document version information at the bottom right corner:
  - "ESP32-S3 TRM (Version 1.7)"
- Link for submitting documentation feedback.

**Navigation Links:**
- GoBack link is provided in blue text on top of each section header, indicating a way to navigate back within this chapter or related sections.