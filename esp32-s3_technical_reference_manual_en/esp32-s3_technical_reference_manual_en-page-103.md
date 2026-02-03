**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Subtitle:**
1.8.27 EE.LDF.64.IP

**Section Title:**
Instruction Word

**Instruction Details Table:**
- 111000
- imm8[7:6]
- fu0[3:0]
- imm8[5:2]
- fu1[3:0]
- O1O
- imm8[0]
- as[3:0]
- I1I
- imm8[1]

**Section Title:**
Assembler Syntax

**Syntax Example:**
EE.LDF.64.IP fu1, fu0, as, -1024..1016

**Section Title:**
Description

**Body Text:**
This instruction forces the lower 3 bits of the access address in register `as` to zero, loads 64-bit data from memory, and stores it in order from low bit to high bit to floating-point registers `fu0` and `fu1`. After the access is completed, the value in register `as` is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 3.

**Section Title:**
Operation

**Body Text with Code Example:**
```
dataIn[63:0] = load64({as[31:3],3{0}})
fu1 = dataIn[63:32]
fu0 = dataIn[31: 0]
as[31:0] = as[31:0] + {21{imm8[7]},imm8[7:0],3{0}}
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback