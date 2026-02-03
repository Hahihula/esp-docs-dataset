**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.29 EE.LDQA.S16.I28.IP

**Instruction Word Breakdown Table:**
- `0`: imm16[7]
- `0`: 0000010
- `imm16[6:0]`: imm16
- `as[3:0]`: as
- `0100`

**Assembler Syntax Example:**
EE.LDQA.S16.I28.IP as, -2048..2032

**Description Section:**
This instruction forces the lower 4 bits of the access address in register as to zero. loads 16-byte data from memory, divides it into 8 segments of 16 bits, sign-extends each segment to 40 bits, and then stores the results to the 160-bit special registers QACC_L and QACC_H respectively. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Operation Section:**
```plaintext
dataIn[127:0] = load128({as[31:4],4{0}})

QACC_L[ 39: 0] = {24[dataIn[15]], dataIn[ 15: 0]}
QACC_L[ 79: 40] = {24[dataIn[31]], dataIn[ 31: 16]}
...
QACC_H[ 39: 0] = {24[dataIn[79]], dataIn[ 79: 64]}
QACC_H[ 79: 40] = {24[dataIn[95]], dataIn[ 95: 80]}
as[31:0] = as[31:0] + {20{imm16[7]}, imm16[7:0],4{0}}
```

**Footer Information:**
Espressif Systems
Page number and document version:
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback