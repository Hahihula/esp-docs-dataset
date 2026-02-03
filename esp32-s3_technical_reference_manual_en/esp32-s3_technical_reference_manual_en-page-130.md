**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Heading:**
1.8.54 EE.SRCMB.S16.QACC

**Subheading - Instruction Word:**
- 11 qu[2:1] 1010 as[3:0] 0100
- 11 qu[0] 1110

**Subheading - Assembler Syntax:**
EE.SRCMB.S16.QACC qu, as, O

**Subheading - Description:**
This instruction extracts 8 data segments of 40 bits from special registers QACC_H and QACC_L and perform arithmetic right shift operations respectively. While writing the shift result back to QACC_H and QACC_L, the instruction saturates the result to 16-bit signed numbers and writes the 8 16-bit data obtained after saturation into register qu.

**Subheading - Operation:**
```
temp0[39:0] = QACC_L[ 39: 0]
...
temp3[39:0] = QACC_L[159:120]
temp4[39:0] = QACC_H[ 39: 0]
...
temp7[39:0] = QACC_H[159:120]

temp_shf0[39:0] = temp0[39:0] >> as[5:0]
temp_shf1[39:0] = temp1[39:0] >> as[5:0]
...
temp_shf7[39:0] = temp7[39:0] >> as[5:0]

QACC_L[ 39: 0] = temp_shf0[39:0]
...
QACC_L[159:120] = temp_shf3[39:0]
QACC_H[ 39: 0] = temp_shf4[39:0]
...
QACC_H[159:120] = temp_shf7[39:0]

qu[ 15: 0] = min(max(temp_shf0[39:0], -2^15), 2^15)-1
...
qu[63:48] = min(max(temp_shf3[39:0], -2^15), 2^15)-1
qu[79:64] = min(max(temp_shf4[39:0], -2^15), 2^15)-1
...
qu[127:112] = min(max(temp_shf7[39:0], -2^15), 2^15)-1
```

**Footer Information:**
Espressif Systems  
Page number: 130  
Document version and type information at the bottom right corner.