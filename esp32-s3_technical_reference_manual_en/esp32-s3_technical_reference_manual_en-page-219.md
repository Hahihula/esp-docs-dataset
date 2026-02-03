**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Number and Name:**
1.8.143 EE.VMULAS.S16.QACC.LD.XP.QUP

**Instruction Word Table:**
- qu[2:1] | qy[0] | qs0[2:0] | qu[0] | qs1[2:0] | qx[1:0] | qs2[2:0] | ad[3:0] | as[3:0]
  - 101101
- 111

**Assembler Syntax:**
EE.VMULAS.S16.QACC.LD.XP.QUP qu, as, ad, qx, qy, qs0, qs1

**Description:**
This instruction divides registers qx and qy into 8 data segments by 16 bits. Then the signed multiplication result of 8 sets of segments is added to the corresponding 40-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 40-bit signed number and then stored to the corresponding 40-bit data segment in QACC_H and QACC_L.

During the operation, the lower 4 bits of the access address in register as are forced to be O, and then the 16-byte data is loaded from the memory to register qu. After the access is completed, the value in register as is incremented by the value in register ad.
At the same time, this instruction also obtains 16-byte unaligned data by concatenating and shifting consecutive aligned data stored in the two registers qs0 and qs1 and stores it to qs0. The shift byte is stored in special register SAR_BYTE.

**Operation:**
```
QACC_L[39:0] = min(max(QACC_L[ 39:0] + qx[ 15:0] * qy[ 15:0] , -2^{39}), 2^{39}-1)
QACC_L[79:40] = min(max(QACC_L[ 79:40] + qx[ 31:16] * qy[ 31:16], -2^{39}), 2^{39}-1)
QACC_L[119:80] = min(max(QACC_L[119:80] + qx[ 47:32] * qy[ 47:32], -2^{39}), 2^{39}-1)
QACC_L[159:120] = min(max(QACC_L[159:120] + qx[ 63:48] * qy[ 63:48], -2^{39}), 2^{39}-1)
QACC_H[39:0] = min(max(QACC_H[ 39:0] + qx[ 79:64] * qy[ 79:64], -2^{39}), 2^{39}-1)
QACC_H[79:40] = min(max(QACC_H[ 79:40] + qx[ 95:80] * qy[ 95:80], -2^{39}), 2^{39}-1)
QACC_H[119:80] = min(max(QACC_H[119:80] + qx[111:96] * qy[111:96], -2^{39}), 2^{39}-1)
QACC_H[159:120] = min(max(QACC_H[159:120] + qx[127:112] * qy[127:112], -2^{39}), 2^{39}-1)

qu[127:0] = load128({as[31:4],4{0}})
as[31:0] = as[31:0] + ad[31:0]
qs0[127:0] = {qs1[127:0], qs0[127:0]} >> {SAR_BYTE[3:0] << 3}
```

**Footer Information:**
Espressif Systems
Page number: 219
Document version and type information:
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback