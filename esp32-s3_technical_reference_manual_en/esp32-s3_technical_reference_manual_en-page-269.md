**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.187 EE.VSMULAS.S16.QACC

**Subsection Titles and Content:**

- **Instruction Word:** 
  - `sel8[2:1]`: 10
  - `sel8[0]`: 1110
  - `qy[2]`: 1
  - `qy[1:0]`: 1 (0)
  - `qx[2:0]`: 11000100

- **Assembler Syntax:** 
  - `EE.VSMULAS.S16.QACC qx, qy, sel8`

- **Description**
  This instruction selects one out of the eight 16-bit data segments in register qy according to immediate number sel8 and performs a signed multiplication on it and the eight 16-bit data segments in register qx respectively. The 8 results obtained are added to the corresponding 40-bit data segment in special registers QACC_H and QACC_L respectively. Then, the result is saturated to a 40-bit signed number and then stored to the corresponding 40-bit data segment in QACC_H and QACC_L.

- **Operation**
  - `temp[15:0] = qy[sel8*16+15:sel8*16]`
  - `QACC_L[39:0] = min(max(QACC_L[39: 0] + qx[15: 0], temp[15:0]), -2^39-1)`
  - `QACC_L[79:40] = min(max(QACC_L[79: 40] + qx[31: 16], temp[15:0]), -2^39)"`
  - `QACC_L[119:80] = min(max(QACC_L[119: 80] + qx[47: 32], temp[15:0]), -2^39)`
  - `QACC_L[159:120] = min(max(QACC_L[159:120] + qx[63: 48], temp[15:0]), -2^39)"`
  - `QACC_H[39:0] = min(max(QACC_H[39: 0] + qx[79: 64], temp[15:0]), -2^39)`
  - `QACC_H[79:40] = min(max(QACC_H[79: 40] + qx[95: 80], temp[15:0]), -2^39)`
  - `QACC_H[119:80] = min(max(QACC_H[119: 80] + qx[111: 96], temp[15:0]), -2^39)`
  - `QACC_H[159:120] = min(max(QACC_H[159:120] + qx[127:112], temp[15:0]), -2^39)`

**Footer Information:** 
- Espressif Systems
- ESP32-S3 TRM (Version 1.7)
- Page number: 269

**Navigation Links:**
- GoBack