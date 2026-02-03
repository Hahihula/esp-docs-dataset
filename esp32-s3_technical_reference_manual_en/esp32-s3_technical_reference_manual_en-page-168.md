**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.92 EE.VLD.L.64.IP

**Subsection - Instruction Word Table:**
- imm8[7]
- qu[2:1]
- 1001
- qu[0]
- imm8[6:0]
- as[3:0]
- 0100

**Subsection Title:**
Assembler Syntax

**Body Text:**
EE.VLD.L.64.IP qu, as, -1024..1016

**Subsection Title: Description**

**Body Text:**
This instruction forces the lower 3 bits of the access address in register as to 0 and loads 64-bit data from memory to the lower 64-bit segment in register qu. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 3.

**Subsection Title: Operation**

**Body Text with Code Block:**
```
1   q[ 63: 0 ] = load64({as[31:3],3{0}})
2   as[31:0] = as[31:0] + {21{imm8[7]},imm8[7:0],3{0}}
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback