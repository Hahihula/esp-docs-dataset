**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Table Header:**
- Instructions
- Description

**Table Content:**

| Instructions | Description |
|--------------|-------------|
| LD.QR       | Load 16-byte data to QR. |
| EE.VLD.128.XP   | Read the 16-byte data, then add the value stored in the AR register to the access address. |
| EE.VLD.128.IP    | Read the 16-byte data, then add the immediate value to the access address. |
| EE.VLD.[H/L].64.XP   | Read the 8-byte data, then add the value stored in the AR register to the access address. |
| EE.VLD.[H/L].64.IP    | Read the 8-byte data, then add the immediate value to the access address. |
| EE.VLDB.[8/16/32]   | Read the 1-byte/2-byte/4-byte data. |
| EE.VLDBC.[8/16/32].XP    | Read the 1-byte/2-byte/4-byte data, then add the value stored in the AR register to the access address. |
| EE.VLDBC.[8/16/32].IP   | Read the 1-byte/2-byte/4-byte data, then add the immediate value to the access address. |
| EE.VLDHBC.16.INCP    | Read the 16-byte data, then add 16 to the access address. |
| EE.LDF.[64/128].XP   | Read the 8-byte/16-byte data, then add the value stored in the AR register to the access address. |
| EE.LDF.[64/128].IP    | Read the 8-byte/16-byte data, then add the immediate value to the access address. |
| EE.LD.128.USAR.XP   | Read the 16-byte data, then add the value stored in the AR register to the access address. |
| EE.LD.128.USAR.IP    | Read the 16-byte data, then add the immediate value to the access address. |
| EE.LDQA.U8.128.[XP/IP]   | Read the 16-byte data and slice it by 1-byte, and zero-extend it to 20-bit data, which then will be written to register QACC_H and QACC_L, and finally add the value stored in the AR register or the immediate value to the access address. |
| EE.LDQA.U16.128.XP   | Read the 16-byte data and slice it by 2-byte, and zero-extend it to 40-bit data, which then will be written to register QACC_H and QACC_L, and finally add the value stored in the AR register or the immediate value to the access address. |
| EE.LDQA.S8.128.XP   | Read the 16-byte data and slice it by 1-byte, then sign-extend it to 20-bit data, which then will be written to register QACC_H and QACC_L, and finally add the value stored in the AR register or the immediate value to the access address. |
| EE.LDQA.S16.128.XP   | Read the 16-byte data and slice it by 1-byte, then sign-extend it to 40-bit data, which then will be written to register QACC_H and QACC_L, and finally add the value stored in the AR register or the immediate value to the access address. |
| EE.LD.QACC_[H/L].H32.IP   | Read the 16-byte data, then add the immediate value to the access address. |
| EE.LD.QACC_[H/L].L128.IPS    | Read the 16-byte data, then add the immediate value to the access address. |
| EE.LD.ACCX.IP   | Read the 8-byte data, then add the immediate value to the access address. |
| EE.LD.UA_STATE.IP   | Read the 16-byte data, then add the immediate value to the access address. |
| EE.LDXQ.32    | Update access address first, then read the 4-byte data. |

**Section Title:**
1.6.2 Write Instructions

**Section Content:**
The write instructions tells the processor to issue a virtual address to access memory based on the AR register that stores the information about access addresses. Most write instructions write memory first then update the...

**Footer Information:**
- Page Number: 54
- Document Title: ESP32-S3 TRM (Version 1.7)
- Submission Link Text: Submit Documentation Feedback