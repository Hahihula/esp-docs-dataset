**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
18.5 EE.CMUL.S16.LD.INCP

**Subsection Headers and Content:**

- **Instruction Word Table:**
  - 110000
    - qu[2:1] | qy[0]
    - 0000
      - qu[0]
      - qx[2:0]
      - qx[1:0]
      - qx[2:1]
      - s16[4:0]
      - as[3:0]
      - qx[2]

- **Assembler Syntax:**
  - EE.CMUL.S16.LD.INCP qu, as, qz, qx, qy, 0..3

- **Description:**
  This instruction performs a 16-bit signed complex multiplication. The range of the immediate number s14 is 0 ~ 7, which specifies the 32 bits in the two QR registers qx and qy for complex multiplication. The real and imaginary parts of complex numbers are stored in the upper 16 bits and lower 16 bits of the 32 bits respectively.
  - During operation:
    - Lower 4 bits of the access address in register as is forced to be zero,
    - Then, a 16-byte data load from memory into register qu. After accessing this value
      - The value stored at the corresponding location (incremented by s16) will replace the original content.

- **Operation:**
  ```assembly
  if s14 == 0:
     qz[15:0] = (qx[15:0] * qy[15:0]) >> SAR[5:0]
     qx[31:16] = (qx[15:0] + qy[15:0]) >> SAR[5:0]
  if s14 == 1:
     qz[79:64] = (qx[79:64] * qy[79:64]) >> SAR[5:0]
     qx[95:80] = (qx[79:64] + qy[95:80]) >> SAR[5:0]
  if s14 == 2:
     qz[127:112] = (qx[111:96] * qy[111:96]) >> SAR[5:0]
  if s14 == 3:
     qz[79:64] = (qx[79:64] + qy[79:64]) >> SAR[5:0]
     qx[95:80] = (qx[79:64] - qy[127:112]) >> SAR[5:0]
  if s14 == 3:
     qu[127:0] = load128({as[31:4],4{0}})
     as[31:0] = as[31:0] + 16
  ```

**Footer Information:**
- Espressif Systems
- Page number and document version:
  - ESP32-S3 TRM (Version 1.7)
- Submit Documentation Feedback