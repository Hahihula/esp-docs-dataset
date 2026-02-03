**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.88 EE.VLD.128.IP

**Subsection - Instruction Word:**
- 1 imm[6:7]
- qu[2:1]
- O011
- qu[0]
- imm[6:0]
- as[3:0]
- O100

**Subsection - Assembler Syntax:**
EE.VLD.128.IP qu, as, -2048..2032

**Subsection - Description:**
This instruction forces the lower 4 bits of the access address in register as to 0 and loads 16-byte data from memory to register qu. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Subsection - Operation:**
```
qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + {20imm16[7]},imm16[7:0],4{0}}
``` 

**Footer Information:**
- Page number 164
- Company name: Espressif Systems
- Document version and title: ESP32-S3 TRM (Version 1.7)
- Link text: Submit Documentation Feedback