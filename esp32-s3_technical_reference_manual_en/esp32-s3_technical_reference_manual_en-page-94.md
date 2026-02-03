**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.18 EE.LD.128.USAR.XP

**Instruction Word Table:**
- qu[2:1]: 10, 1101
- qu[0]: 00
- ad[3:0]: 
- as[3:0]: 
- o100: 

**Assembler Syntax:**
EE.LD.128.USAR.XP qu, as, ad

**Description:**
This instruction forces the lower 4 bits of the access address in register as to 0 and loads 16-byte data from memory to register qu. Meanwhile, it saves the value of the lower 4 bits in as to the special register SAR_BYTE. After the access is completed, the value in register as is incremented by the value in register ad.

**Operation:**
```
qu[127:0] = load128(as[31:4],4{0})
SAR_BYTE = as[3:0]
as[31:0] = as[31:0] + ad[31:0]
``` 

**Footer Information:**
Espressif Systems
94 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback