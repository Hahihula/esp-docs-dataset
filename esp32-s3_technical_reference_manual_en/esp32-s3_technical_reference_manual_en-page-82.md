**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
18.6 EE.CMUL.S16.ST.INCP

**Subsection Headers and Content:**

- **Instruction Word:** 
  - 1100100 | qy[0] | qv[2:0] | 0 | qz[2:0] | qx[1:0] | qy[2:1] | OO | sel4[1:0] | as[3:0] | 111 | qx[2]

- **Assembler Syntax:** 
  - EE.CMUL.S16.ST.INCP qv, as, qz, qx, qy, sel4

- **Description:**
  This instruction performs a 16-bit signed complex multiplication. The range of the immediate number `sel4` is from 0 to ~7, which specifies the 32 bits in the two QR registers `qx` and `qy` for complex multiplication. The real and imaginary parts of complex numbers are stored in the upper 16 bits and lower 16 bits respectively.

- **Operation:**
  - During operation:
    - The calculated real part and imaginary part results are stored in the corresponding 32 bits of register `qz`.
    - If `sel4` is zero, then stores the 16-byte data of `qv` to memory. After access, incrementing by 16.
  
- **Code Block:**
  ```assembly
  if sel4 == 0:
      qz[ 75: 0] = (qx[ 15: 0] * qy[ 15: 0] - qx[ 31: 16]) >> SAR[5:0]
      qz[ 31: 16] = (qx[ 15: 0] * qy[ 31: 16] + qx[ 31: 16]) >> SAR[5:0]
      qz[47: 32] = (qx[ 47: 32] * qy[ 47: 32] - qx[ 63: 48]) >> SAR[5:0]
      qz[63: 48] = (qx[ 47: 32] * qy[ 63: 48] + qx[ 63: 48]) >> SAR[5:0]

  if sel4 == 1:
      qz[ 79: 64] = (qx[ 79: 64] * qy[ 79: 64] - qx[ 95: 80]) >> SAR[5:0]
      qz[ 95: 80] = (qx[ 95: 80] * qy[ 95: 80] + qx[ 79: 64]) >> SAR[5:0]
      qz[127:112] = (qx[127:112] * qy[127:112] - qx[127:112]) >> SAR[5:0]

  if sel4 == 2:
      qz[ 15: 0] = (qx[ 15: 0] * qy[ 15: 0] + qx[ 31: 16]) >> SAR[5:0]
      qz[ 31: 16] = (qx[ 31: 16] * qy[ 31: 16] - qx[ 47: 32]) >> SAR[5:0]
      qz[47: 32] = (qx[ 47: 32] * qy[ 47: 32] + qx[ 47: 32]) >> SAR[5:0]
      qz[63: 48] = (qx[ 63: 48] * qy[ 63: 48] - qx[ 63: 48]) >> SAR[5:0]

  if sel4 == 3:
      qz[ 79: 64] = (qx[ 79: 64] * qy[ 79: 64] + qx[ 95: 80]) >> SAR[5:0]
      qz[ 95: 80] = (qx[ 95: 80] * qy[ 95: 80] - qx[ 79: 64]) >> SAR[5:0]
      qz[127:112] = (qx[127:112] * qy[127:112] + qx[127:112]) >> SAR[5:0]

  if sel4 == 3:
      qz[ 79: 64] = (qx[ 79: 64] * qy[ 79: 64] - qx[ 95: 80]) >> SAR[5:0]
      qz[ 95: 80] = (qx[ 95: 80] * qy[ 95: 80] + qx[ 79: 64]) >> SAR[5:0]
      qz[127:112] = (qx[127:112] * qy[127:112] - qx[127:112]) >> SAR[5:0]

  qv[127:0] => store128({as[31:4],4{0}})
  as[31:0] = as[31:0] + 16
  ```

**Footer Information:** 
- Page number and document version:
  - "Espressif Systems" | page 82 | ESP32-S3 TRM (Version 1.7)
  
**Navigation Links:**
- Submit Documentation Feedback