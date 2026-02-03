**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.55 EE.SRCMB.S8.QACC

**Instruction Word Table:**
- qu[2:1]: 011
- qu[0]: 1111
- as[3:0]: 0100 (highlighted in blue)

**Assembler Syntax:**
EE.SRCMB.S8.QACC qu, as, O

**Description:**
This instruction extracts 16 data segments of 20 bits from special registers QACC_H and QACC_L and performs arithmetic right shift operations respectively. While writing the shift result back to QACC_H and QACC_L, the instruction saturates the result to 8-bit signed numbers and writes the 16 8-bit data obtained after saturation into register qu.

**Operation:**
```
temp0[19:0] = QACC_L [ 19: 0]
temp1[19:0] = QACC_L [39:20]
...
temp7[19:0] = QACC_L[159:140]
temp8[19:0] = QACC_H [ 19: 0]
temp9[19:0] = QACC_H [39:20]
...
temp15[19:0] = QACC_H[159:140]

temp_shf0[19:0] = temp0[19:0] >> as[4:0]
temp_shf1[19:0] = temp1[19:0] >> as[4:0]
...
temp_shf15[19:0] = temp15[19:0] >> as[4:0]

QACC_L [ 19: 0] = temp_shf0[19:0]
...
QACC_L[159:140] = temp_shf7[19:0]
QACC_H[ 19: 0] = temp_shf8[19:0]

QACC_H[159:140] = temp_shf15[19:0]

qu [ 7 : 0 ] = min(max(temp_shf0[19:0], -2^7), 2^7-1)
qu [ 15 : 8 ] = min(max(temp_shf1[19:0], -2^7), 2^7-1)
...
qu [63 : 56] = min(max(temp_shf7[19:0], -2^7), 2^7-1)
qu [71 : 64] = min(max(temp_shf8[19:0], -2^7), 2^7-1)
qu [79 : 72] = min(max(temp_shf9[19:0], -2^7), 2^7-1)
...
qu[127:120] = min(max(temp_shf15[19:0], -2^7), 2^7-1)
```

**Footer Information:**
Espressif Systems
Page number: 131
Document version and title: ESP32-S3 TRM (Version 1.7)

**Navigation Link:** 
GoBack