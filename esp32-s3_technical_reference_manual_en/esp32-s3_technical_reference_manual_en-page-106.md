**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.30 EE.LDQA.S16.128.XP

**Subsection - Instruction Word:**
- Binary representation of the instruction word is shown as `01111100100 ad[3:0] as[3:0] 0100`.

**Subsection - Assembler Syntax:**
- The syntax for this instruction in assembly language is given by:
  ```
  EE.LDQA.S16.128.XP as, ad
  ```

**Subsection - Description:**
This description explains the operation of the `EE.LDQA.S16.128.XP` instruction:

- The lower four bits (bits [3:0]) from an access address in register `as` are used to load a memory location.
- This 4-bit portion is divided into eight segments, each segment being extended by sign-extension of the remaining three higher-order bits and then stored as part of two special registers (`QACC_L` at bit positions [39:0] with data from `[127:80]`, `QACC_H` at bit positions [39:0] to [64:0] for segments 5-8, etc.).
- After the access is completed and all eight memory locations have been loaded into their respective registers (`QACC_L` & `QACC_H`), each segment's value in register `as` will be incremented by one.

**Subsection - Operation (Code Block):**
The operation of this instruction can also be represented as a series of code blocks:

```
dataIn[127:0] = load128({as[31:4], 4{0}})
QACC_L[ 39: ] = {24{dataIn[15]}, dataIn[ 15: 0]}
QACC_L[ 79:40] = {24{dataIn[31]}, dataIn[ 31: 16]}
...
QACC_H[ 39: 0 ] = {24{dataIn[79]}, dataIn[ 79: 64]}
QACC_H[ 79: 40] = {24{dataIn[95]}, dataIn[ 95: 80]}
as[31:0] = as[31:0] + ad[31:0]
```

**Footer Information:**
- Company Name: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Page Number: 106

**Navigation Links:**
- GoBack button at the top right corner.
- Submit Documentation Feedback link available on page footer.

This document provides a detailed explanation of how to use the `EE.LDQA.S16.128.XP` instruction in processor programming, including its syntax and operation steps with code examples for clarity.