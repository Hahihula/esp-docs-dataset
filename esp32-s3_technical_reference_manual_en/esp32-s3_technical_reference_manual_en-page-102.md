**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.26 EE.LDF.128.XP

**Instruction Word Table:**
- 10001
- fu3[3:1]
- fu0[3:0]
- fu3[0]
- fu2[3:1]
- fu1[3:0]
- ad[3:0]
- as[3:0]
- 111
- fu2[0]

**Assembler Syntax Heading:**
Assembler Syntax

**Syntax Description:**
EE.LDF.128.XP fu3, fu2, fu1, fu0, as, ad

**Description Section:**
This instruction forces the lower 4 bits of the access address in register as to zero, loads 16-byte data from memory, and stores it in order from low bit to high bit to floating-point registers fu0, fu1, fu2, and fu3. After the access is completed, the value in register as is incremented by the value in register ad.

**Operation Section:**
- `dataIn[127:0] = load128({as[31:4], 4{0}})`
- `fu3 = dataIn[127: 96]`
- `fu2 = dataIn[ 95: 64]`
- `fu1 = dataIn[ 63: 32]`
- `fu0 = dataIn[ 31:   0]`
- `as[31:0] = as[31:0] + ad[31:0]`

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback