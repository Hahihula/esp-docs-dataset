**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.116 EE.VMIN.S32

**Instruction Word Table:**
- `10`
- `qa[2:1]`: `1110`
- `qa[0]`: `0`
- `qy[2]`: `1`
- `qy[1:0]`: `0`
- `qx[2:0]`: `01100100`

**Subheader - Assembler Syntax:**
EE.VMIN.S32 qa, qx, qy

**Subheader - Description:**
This instruction compares numerical values of the four 32-bit vector data segments in registers qx and qy. The data segment with the smaller value is written into the corresponding 32-bit data segment in register qa.

**Subheader - Operation (List):**
1. `qa[ 31: 0 ] = (qx[ 31: 0 ] <= qy[ 31: 0 ]) ? qx[ 31: 0 ] : qy[ 31: 0 ]`
2. `qa[63: 32] = (qx[ 63: 32] <= qy[ 63: 32 ]) ? qx[ 63: 32 ] : qy[ 63: 32 ]`
3. ...
4. `qa[127:96] = (qx[127:96] <= qy[127:96]) ? qx[127:96] : qy[127:96]`

**Footer Information:**
Espressif Systems
Page Number: 192
Document Title: ESP32-S3 TRM (Version 1.7)
Link Texts:
- Submit Documentation Feedback