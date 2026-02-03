Title: Chapter 1 Processor Instruction Extensions (PIE)

Subtitle: GoBack

Section Title:
1.8.126 EE.VMUL.S8.LD.INCP

Subsection Titles and Content:

Instruction Word Table:
- qu[2:1] | qy[0] | 100 | qu[0] | qz[2:0] | qx[1:0] | qy[2:1] | as[3:0] | 111 | qx[2]

Assembler Syntax:
EE.VMUL.S8.LD.INCP qqu, as, qx, qx, qy

Description
This instruction performs a signed vector multiplication on 8-bit data. Registers qx and qy are the multiplier and multiplicand respectively. The 16 bit-data results obtained from the calculation is arithmetically right-shifted by the value in special register SAR. Then, the lower 8-bit data of the shift result is written into corresponding segment of register qx.

During the operation, the lower 4 bits of the address access in register as are forced to be O, and then the 16-byte data is loaded from the memory to register qu. After the access, the value in register as is incremented by 16.

Operation
- qz[7:0] = (qx[7:0] * qx[7:0]) >> SAR[5:0]
- qz[15:8] = (qx[15:8] * qx[15:8]) >> SAR[8:]
- qz[23:16] = (qx[23:16] * qx[23:16]) >> SAR[16:]
- qz[31:24] = (qx[31:24] * qx[31:24]) >> SAR[24:]
- qz[39:32] = (qx[39:32] * qx[39:32]) >> SAR[32:]
- qz[47:40] = (qx[47:40] * qx[47:40]) >> SAR[40:]
- qz[55:48] = (qx[55:48] * qx[55:48]) >> SAR[48:]
- qz[63:56] = (qx[63:56] * qx[63:56]) >> SAR[56:]
- qz[71:64] = (qx[71:64] * qx[71:64]) >> SAR[64:]
- qz[79:72] = (qx[79:72] * qx[79:72]) >> SAR[72:]
- qz[87:80] = (qx[87:80] * qx[87:80]) >> SAR[80:]
- qz[95:88] = (qx[95:88] * qx[95:88]) >> SAR[88:]
- qz[103:96] = (qx[103:96] * qx[103:96]) >> SAR[96:]
- qz[111:104] = (qx[111:104] * qx[111:104]) >> SAR[104:]
- qz[119:112] = (qx[119:112] * qx[119:112]) >> SAR[112:]
- qz[127:120] = (qx[127:120] * qx[127:120]) >> SAR[120:]

qu[127:0] = load128({as[31:4], 4{0}})

as[31:0] = as[31:0]

Footer:
Espressif Systems
Page Number and Document Version Information (centered at the bottom):
ESP32-S3 TRM (Version 1.7)