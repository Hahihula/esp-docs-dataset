**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.84 EE.VCMP.GT.S8

**Instruction Word Table:**
- `10`
- `qa[2:1]`: `1110`
- `qa[0]`: `0`
- `qy[2]`: `0`
- `qy[1:0]`: `0`
- `qx[2:0]`: `11100100`

**Assembler Syntax Section:**
- **Title:** Assembler Syntax
- **Syntax Example:** EE.VCMP.GT.S8 qa, qx, qy

**Description Section:**
- This instruction compares 8-bit vector data. It compares the numerical values of the 16 8-bit data segments in registers qx and qy. If the former is larger than the latter, it writes `0xFF` into the corresponding 8-bit data segment in register qa. Otherwise, it writes `0` to the segment.

**Operation Section:**
- **Title:** Operation
- **Instructions List (formatted as code):**
  ```
  1   qa[7]: 0 = (qx[7] > qy[7]) ? 0x{FF} : 0
  2   qa[15:8] = (qx[15:8] > qy[15:8]) ? 0x{FF} : 0
  ...
  4   qa[127:120] = (qx[127:120] > qy[127:120]) ? 0x{FF} : 0
  ```

**Footer Information:**
- "Espressif Systems"
- Page number and document version information:
  - `Page 160`
  - `ESP32-S3 TRM (Version 1.7)`
- Link for submitting documentation feedback.

**Navigation Links:**
- GoBack

(Note: The text in the image is structured as a combination of sections with titles, tables, and lists formatted to resemble code snippets.)