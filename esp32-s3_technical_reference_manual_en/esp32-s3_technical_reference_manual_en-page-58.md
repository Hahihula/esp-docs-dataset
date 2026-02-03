**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Table Header:**
Table 1.6-7. Vector Complex Multiplication Instructions

| Instructions | Description |
|--------------|-------------|
| EE.CMUL.S16 | Perform vector complex multiplication operation to 2-byte data. |
| EE.CMUL.S16.LD.INCP | Perform vector complex multiplication operation to 2-byte data, and read 16-byte data from memory at the same time. |
| EE.CMUL.S16.ST.INCP | Perform vector complex multiplication operation to 2-byte data, and write 16-byte data to memory at the same time. |

**Subheading:**
Vector Multiplication Accumulation Instructions

**Body Text:**
ESP32-S3 provides two types of vector multiplication accumulation instructions: one is based on the ACCX register, accumulating multiple vector multiplication results to a 40-bit ACCX register; and the other is based on QACC_H and QACC_L registers, accumulating vector multiplication results to the corresponding bit segments of QACC_H and QACC_L registers respectively. Both types of above-mentioned instructions support multiplication accumulation on 1-byte and 2-byte segments.

In order to reduce extra operations as reading memory and improve the speed of code execution, vector multiplication accumulation instructions are designed to perform the multiplication accumulation and access 16 bytes at the same time, and the access address is increased by the value in the AR register or by the immediate value after the access.

In addition, instructions with the "QUP" suffix in the vector multiplication accumulation instructions also support extracting 16-byte aligned data from the unaligned address.

**Table Header:**
Table 1.6-8. Vector Multiplication Accumulation Instructions

| Instructions | Description |
|--------------|-------------|
| EE.VMULAS.[U/S][8/16].ACCX | Perform vector multiplication accumulation to signed/un-signed data in 1-byte/2-byte segment, and store the result to the ACCX register temporarily. |
| EE.VMULAS.[U/S][8/16].ACCX.L.D.IP | Perform vector multiplication accumulation to signed/un-signed data in 1-byte/2-byte segment, and store the result to the ACCX register temporarily, then read 16-byte data from memory. Add immediate to address register. |
| EE.VMULAS.[U/S][8/16].ACCX.L.D.XP | Perform vector multiplication accumulation to signed/un-signed data in 1-byte/2-byte segment, and store the result to the ACCX register temporarily, then read 16-byte data from memory. Add the value of AR register to address register. |
| EE.VMULAS.[U/S][8/16].ACCX.L.D.IP.QUP | Perform vector multiplication accumulation to signed/un-signed data in 1-byte/2-byte segment, and store the result to the ACCX register temporarily. Then read 16-byte data from memory and output a 16-byte aligned data. Add immediate to address register.

**Footer:**
Espressif Systems
Page number: 58
Document version: ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback