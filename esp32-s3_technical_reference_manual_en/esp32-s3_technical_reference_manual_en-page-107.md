**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.31 EE.LDQA.S8.128.IP

**Instruction Word Table:**
- `imm16[7]`: 0
- `imm16[6:0]`: 0000
- `as[3:0]`: 0100

**Assembler Syntax Section:**
- **Title:** Assembler Syntax
- **Syntax Example:** EE.LDQA.S8.128.IP as, -2048..2032

**Description Section:**
- This instruction forces the lower 4 bits of the access address in register `as` to zero, loads 16-byte data from memory, divides it into 16 segments of 8 bits, sign-extends each segment to 20 bits, and then stores the results to the 160-bit special registers QACC_L and QACC_H respectively. After the access is completed, the value in register `as` is incremented by an 8-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Operation Section:**
- **Title:** Operation
- **Code Block:**
```
dataIn[127:0] = load128({as[31:4],4{0}})
QACC_L[19:0] = {12[dataIn[7], dataIn[7:0]]
QACC_L[39:20] = {12[dataIn[15], dataIn[15:8]]
...
QACC_H[159:140] = {12[dataIn[127], dataIn[127:120]]
as[31:0] = as[31:0] + {20{imm16[7]}, imm16[7:0], 4{0}}
```

**Footer Information:**
- Espressif Systems
- Page Number: 107
- Document Title: ESP32-S3 TRM (Version 1.7)
- Link Texts:
  - Submit Documentation Feedback