**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
18.4 EE.CMUL.S16

**Instruction Word:**
- 10 | qz[2:1] 1110 | qz[0] | qy[2] 0 | qy[1:0] | qx[2:0] 0O | sel4[1:0] 0100

**Assembler Syntax:**
EE.CMUL.S16 qz, qx, qy, 0..3

**Description:**
This instruction performs a 16-bit signed complex multiplication. The range of the immediate number se14 is 0 ~ 3, which specifies the 32 bits in the two QR registers qx and qy for complex multiplication. The real and imaginary parts of complex numbers are stored in the upper 16 bits and lower 16 bits of the 32 bits respectively.

The calculated real part and imaginary part results are stored in the corresponding 32 bits of register qz.

**Operation:**
```
if sel4 == 0:
    qz[ 15: 0 ] = (qx[ 15: 0 ] * qy[ 15: 0 ]) - qx[ 31: 16 ] * qy[ 31: 16 ] >> SAR[5:0]
qz[ 31: 16 ] = (qx[ 15: 0 ] * qy[ 31: 16 ] + qx[ 31: 16 ] * qy[ 15: 0 ]) >> SAR[5:0]
qz[ 47: 32 ] = (qx[ 47: 32 ] * qy[ 47: 32 ] - qx[ 63: 48 ] * qy[ 47: 32 ]) >> SAR[5:0]
qz[ 63: 48 ] = (qx[ 63: 48 ] * qy[ 63: 48 ] + qx[ 47: 32 ] * qy[ 15: 0 ]) >> SAR[5:0]

if sel4 == 1:
    qz[ 79: 64 ] = (qx[ 79: 64 ] * qy[ 79: 64 ] - qx[ 95: 80 ] * qy[ 95: 80 ]) >> SAR[5:0]
    qz[ 95: 80 ] = (qx[ 95: 80 ] * qy[ 79: 64 ] + qx[ 79: 64 ] * qy[ 15: 0 ]) >> SAR[5:0]
    qz[111: 96 ] = (qx[111: 96 ] * qy[111: 96 ] - qx[127:112 ] * qy[127:112 ]) >> SAR[5:0]
    qz[127:112] = (qx[127:112 ] * qy[127:112 ] + qx[ 95: 80 ] * qy[ 47: 32 ]) >> SAR[5:0]

if sel4 == 2:
    qz[ 15: 0 ] = (qx[ 15: 0 ] * qy[ 15: 0 ] + qx[ 31: 16 ] * qy[ 31: 16 ]) >> SAR[5:0]
    qz[ 31: 16 ] = (qx[ 31: 16 ] * qy[ 31: 16 ] + qx[ 47: 32 ] * qy[ 15: 0 ]) >> SAR[5:0]
    qz[ 47: 32 ] = (qx[ 47: 32 ] * qy[ 47: 32 ] + qx[ 63: 48 ] * qy[ 15: 0 ]) >> SAR[5:0]
    qz[ 63: 48 ] = (qx[ 63: 48 ] * qy[ 63: 48 ] + qx[ 79: 64 ] * qy[ 15: 0 ]) >> SAR[5:0]
    qz[ 79: 64 ] = (qx[ 79: 64 ] * qy[ 79: 64 ] + qx[ 95: 80 ] * qy[ 15: 0 ]) >> SAR[5:0]
    qz[ 95: 80 ] = (qx[ 95: 80 ] * qy[ 79: 64 ] + qx[ 79: 64 ] * qy[ 15: 0 ]) >> SAR[5:0]
    qz[111: 96 ] = (qx[111: 96 ] * qy[111: 96 ] + qx[ 95: 80 ] * qy[ 47: 32 ]) >> SAR[5:0]
    qz[127:112] = (qx[127:112 ] * qy[127:112 ] + qx[ 95: 80 ] * qy[ 47: 32 ]) >> SAR[5:0]

if sel4 == 3:
    qz[ 79: 64 ] = (qx[ 79: 64 ] * qy[ 79: 64 ] + qx[ 95: 80 ] * qy[ 15: 0 ]) >> SAR[5:0]
    qz[ 95: 80 ] = (qx[ 95: 80 ] * qy[ 79: 64 ] + qx[ 79: 64 ] * qy[ 15: 0 ]) >> SAR[5:0]
    qz[111: 96 ] = (qx[111: 96 ] * qy[111: 96 ] + qx[ 95: 80 ] * qy[ 47: 32 ]) >> SAR[5:0]
    qz[127:112] = (qx[127:112 ] * qy[127:112 ] + qx[ 95: 80 ] * qy[ 47: 32 ]) >> SAR[5:0]
```

**Footer Information:**
- Page number: 80
- Document version and title: ESP32-S3 TRM (Version 1.7)
- Company name: Espressif Systems

**Navigation Links:**
- GoBack button at the top right corner.
- Submit Documentation Feedback link at the bottom center.

(Note: The code block is a representation of an assembly instruction set, not actual source code.)