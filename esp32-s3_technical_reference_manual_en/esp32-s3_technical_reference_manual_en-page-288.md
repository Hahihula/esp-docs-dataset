**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.205 EE.VSUSB.S8.LD.INCP

**Subsection Titles and Content:**

- **Instruction Word:** 
  - `111000`
  - `qu[2:1]`: `qy[0]` : `110`
  - `qu[0]`: `qa[2:0]`: `qx[1:0]`: `qy[2:1]`: `as[3:0]`: `111`
  - `qx[2]`

- **Assembler Syntax:** 
  - `EE.VSUSB.S8.LD.INCP qu, as, qax, qx, qay`

- **Description**
  This instruction performs a vector subtraction on 8-bit data. Registers `qax` and `qay` are the subtrahend and the minuend respectively. Then, the 16 results obtained from the calculation are saturated and then written into register `qa`.

During the operation, the lower 4 bits of the access address in register `as` are forced to be zero (`0`), and then the 16-byte data is loaded from memory to register `qu`. After the access, the value in register `as` is incremented by 16.

- **Operation**
```
qa[7:0] = min(max(qx[7:0] - qy[7:0], -2^7), 2^7) - 1
qa[15:8] = min(max(qx[15:8] - qy[15:8], -2^7), 2^7) - 1

qu[127:0] = load128({as[31:4], 4{0}})
as[31:0] = as[31:0] + 16
```

**Footer Information:** 
- Page number and document version:
  - "Espressif Systems"
  - "ESP32-S3 TRM (Version 1.7)"
  
- Navigation Links:
  - GoBack

- Document Feedback Link:
  - Submit Documentation Feedback