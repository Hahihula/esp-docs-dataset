**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.93 EE.VLD.L.64.XP

**Subheading - Instruction Word:**
- 10 qu[2:1] 1101
- 011 ad[3:0] as[3:0]
- 0100

**Subheading - Assembler Syntax:**
EE.VLD.L.64.XP qu, as, ad

**Subheading - Description:**
This instruction forces the lower 3 bits of the access address in register as to 0 and loads 64-bit data from memory to the lower 64-bit segment in register qu. After the access is completed, the value in register as is incremented by the value in register ad.

**Subheading - Operation:**
```
1   q[ 63: 0 ] = load64({as[31:3],3{0}})
2   a[31:0] = a[31:0] + ad[31:0]
``` 

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback