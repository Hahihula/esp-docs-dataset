**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.39 EE.MOV.S8.QACC

**Instruction Word Table:**
- **Instruction Word:** 
  - `11 qs[2:1]` | `1101 qs[0]` | `111111100110100`

**Subsection Title:**
Assembler Syntax

**Syntax Example:**
EE.MOV.S8.QACC qs

**Description Section:**
This instruction sign-extends the 16 segments of 8-bit data in the register qs to 20 bits and writes the result to special registers QACC_H and QACC_L.

**Operation Table:**

| Operation | Description |
|-----------|-------------|
| `QACC_L[ 19 : 0 ] = {12[qs[7]], qs[ 7 : 0 ]}` | |
| `QACC_L[ 39 : 20 ] = {12[qs[15]], qs[ 15 : 8 ]}` | |
| `QACC_H[159:140] = {12[qs[127]], qs[127:120]}` | |

**Footer Information:**
- Page Number: 115
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems

**Link Texts:**
- GoBack
- Submit Documentation Feedback