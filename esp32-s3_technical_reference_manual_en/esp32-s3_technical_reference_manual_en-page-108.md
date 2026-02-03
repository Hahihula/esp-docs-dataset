**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.32 EE.LDQA.S8.128.XP

**Subsection - Instruction Word:**
- Binary representation of the instruction word is shown as `0111000100 ad[3:0] as[3:0] 0100`.

**Subsection - Assembler Syntax:**
- The syntax for this instruction in assembly language.

**Subsection - Description:**
This instruction forces the lower 4 bits of the access address in register `as` to zero, loads 16-byte data from memory, divides it into two segments each with a length corresponding to an 8-bit bit width. Sign-extends (each segment is sign-extended) and then stores these results as special registers QACC_L and QACC_H respectively.

**Subsection - Operation:**
A block of code illustrating the operation:
```
dataIn[127:0] = load128({as[31:4], 4{0}})
QACC_L[19:0] = {12[dataIn[7]], dataIn[7:0]}
QACC_L[39:20] = {12[dataIn[15]], dataIn[15:8]}
...
QACC_H[159:140] = {12[dataIn[127]], dataIn[127:120]}
as[31:0] = as[31:0] + ad[31:0]
```

**Footer Information:**
- Company name and logo at the bottom left.
- Page number 108
- Document version information (ESP32-S3 TRM, Version 1.7)
- Links for "Submit Documentation Feedback"