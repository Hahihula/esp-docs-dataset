**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.40 EE.MOV.U16.QACC

**Subsection Titles and Content:**

- **Instruction Word:** 
  - `11 qs[2:1] 1101 qs[0] 111111101100100`

- **Assembler Syntax**
  - `EE.MOV.U16.QACC qs`

- **Description**
  - This instruction zero-extends the 8 segments of 16-bit data in register qs to 40 bits and writes the result to special registers QACC_H and QACC_L.

- **Operation Table:**

  | Operation | Description |
  |-----------|-------------|
  | `QACC_L[39: 0] = {24(0), qs[15: 0]}` | Zero-extension of the lower segment. |
  | `QACC_L[79: 40] = {24(0), qs[31: 16]}` | Zero-extension from the middle to upper segments. |
  | `QACC_L[119:80] = {24(0), qs[47:32]}` | Zero-extension of the lower segment in reverse order (from right). |
  | `QACC_L[159:120] = {24(0), qs[63:48]}` | Zero-extension from middle to upper segments. |

  | Operation | Description |
  |-----------|-------------|
  | `QACC_H[39: 0] = {24(0), qs[79: 64]}` | Zero-extension of the lower segment in reverse order (from right). |
  | `QACC_H[79:40] = {24(0), qs[95:80]}` | Zero-extension from middle to upper segments. |
  | `QACC_H[119:80] = {24(0), qs[111:96]}` | Zero-extension of the lower segment in reverse order (from right). |
  | `QACC_H[159:120] = {24(0), qs[127:112]}` | Zero-extension from middle to upper segments. |

**Footer Information:** 
- Espressif Systems
- Page number and document version information at the bottom right corner:
  - "116 ESP32-S3 TRM (Version 1.7)"
- Link for submitting documentation feedback: `Submit Documentation Feedback`