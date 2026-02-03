**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.58 EE.SRS.ACCX

**Subheader - Instruction Word:**
01111100 | 001 au[3:0] as[3:0] 0100

**Subheader - Assembler Syntax:**
EE.SRS.ACCX au, as, O

**Subheader - Description:**
This instruction performs an arithmetic right shift on special register ACCX. While writing the shift result back to ACCX, the instruction saturates shift result to a 32-bit signed number and writes the saturated result into register au.

**Subheader - Operation (with code block):**
```
temp_shf[39:0] = ACCX[39:0] >> as[5:0]
ACCX = temp_shf[39:0]
au = min(max(temp_shf[39:0], -2^{31}), 2^{31}-1)
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)

**Navigation Link:**
GoBack

**Page Number and Feedback Option:**
Submit Documentation Feedback