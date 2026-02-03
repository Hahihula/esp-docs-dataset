**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.50 EE.SRC.Q.LD.IP

**Subheading - Instruction Word:**
Instruction Word  
111000 | imm16[7:6] | imm16[2] | qs1[2:0] | imm16[5] | qu[2:0] | qs0[1:0] | imm16[4:3] | 00 | imm16[1:0] | as[3:0] | 111 | qs0[2]

**Subheading - Assembler Syntax:**
Assembler Syntax  
EE.SRC.Q.LD.IP qu, as, -2048..2032, qs0, qs1

**Subheading - Description:**
Description  
This instruction performs an arithmetic right shift on the 32-byte concatenation of registers qs0 and qs1 that hold the loaded data of two consecutive aligned addresses. By this way, you can obtain unaligned 16-byte data, which will be written to register qs0. The right shift amount is SAR_BYTE multiplied by 8.

At the same time, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access is completed, the value in register as is incremented by 8-bit sign-extended constant in the instruction code segment left-shifted by 4.

**Subheading - Operation:**
Operation  
```
qs0[127:0] = {qs1[127:0], qs0[127:0]} >> {SAR_BYTE[3:0] << 3}
qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + {20{imm16[7]}, imm16[7:0],4{0}}
```

**Footer Information:**  
Espressif Systems  
Page number 126  
ESP32-S3 TRM (Version 1.7)  

**Link - Submit Documentation Feedback**: 
GoBack