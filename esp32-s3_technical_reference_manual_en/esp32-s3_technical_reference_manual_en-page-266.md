**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.184 EE.VRELU.S16

**Subheader - Instruction Word:**
- qs[2:1] = 1101, qs[0] = 001, ax[3:0] = ay[3:0] = O100

**Subheader - Assembler Syntax:**
EE.VRELU.S16 qs, ax, ay

**Subheader - Description:**
This instruction divides register qs into 8 data segments by 16 bits. If the value of the segment is not greater than 0, it will be multiplied by the value of the lower 16 bits in register ax and right-shifted by the value of the lower 6 bits in register ay, and then the result obtained will overwrite the value of the segment. Otherwise, the value of the segment will remain unchanged.

**Subheader - Operation:**
```
qs[ 15: 0 ] = ( qs[ 15: 0 ] <= 0 ) ? ( qs[ 15: 0 ] * ax[15:0] ) >> ay[5:0] : qs[ 15: 0 ]
qs [ 31: 16 ] = ( qs[ 31: 16 ] <= 0 ) ? ( qs[ 31: 16 ] * ax[15:0] ) >> ay[5:0] : qs[ 31: 16 ]
...
qs[127:112] = ( qs[127:112] <= 0 ) ? ( qs[127:112] * ax[15:0] ) >> ay[5:0] : qs[127:112]
```

**Footer Information:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback