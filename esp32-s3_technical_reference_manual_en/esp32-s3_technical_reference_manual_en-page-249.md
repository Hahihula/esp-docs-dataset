**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Number and Name:**
18.67 EE.VMULAS.U16.QACC.LD.XP.QUP

**Instruction Word Table:**
- qu[2:1] : qy[0]
- qs0[2:0] : qs1[2:0]
- qu[0]  : qx[1:0]
- qs0[1:0] : qx[2:1]
- ad[3:0] : as[3:0]
- as[3:0] : qx[2]

**Assembler Syntax:**
EE.VMULAS.U16.QACC.LD.XP.QUP qu, as, ad, qx, qy, qs0, qs1

**Description:**
This instruction divides registers qx and qy into 8 data segments by 16 bits. Then, the unsigned multiplication result of the 8 sets of segments is added to the corresponding 40-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 40-bit unsigned number and then stored to the corresponding 40-bit data segment in QACC_H and QACC_L.

During the operation, the lower 4 bits of the access address in register as are forced to be 0, and then the 16-byte data is loaded from the memory to register qu. After the access is completed, the value in register as is incremented by the value in register ad.
At the same time, this instruction also obtains 16-byte unaligned data by concatenating and shifting consecutive aligned data stored in the two registers qs0 and qs1 and stores it to qs0. The shift byte is stored in special register SAR_BYTE.

**Operation:**
```
QACC_L[39:0] = min(QACC_L[39:0] + qx[15:0] * qy[15:0], 2^{40}-1)
QACC_L[79:40] = min(QACC_L[79:40] + qx[31:16] * qy[31:16], 2^{40}-1)
...
QACC_L[159:120] = min(QACC_L[159:120] + qx[63:48] * qy[63:48], 2^{40}-1)
QACC_H[39:0] = min(QACC_H[39:0] + qx[79:64] * qy[79:64], 2^{40}-1)
QACC_H[79:40] = min(QACC_H[79:40] + qx[95:80] * qy[95:80], 2^{40}-1)
...
QACC_H[159:120] = min(QACC_H[159:120] + qx[127:112] * qy[127:112], 2^{40}-1)

qu[127:0] = load(8[as[31:4],4{0}])
as[31:0] = as[31:0] + ad[31:0]
qs0[127:0] = {qs1[127:0], qs0[127:0]} >> 3
```

**Footer Information:**
Espressif Systems  
Page Number: 249  
Document Title: ESP32-S3 TRM (Version 1.7)  
Link Texts:
- GoBack
- Submit Documentation Feedback