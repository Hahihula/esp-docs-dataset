**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Header:**
1.8.153 EE.VMULAS.S8.QACC.LD.IP.QUP

**Instruction Word Table:**
- 0011
- imm16[5:4]
- qu[2:1]
- qy[0]
- qs0[2:0]
- qu[0]
- qs1[2:0]
- qx[1:0]
- qx[2:1]
- imm16[3:0]
- as[3:0]
- 111
- qx[2]

**Assembler Syntax Table:**
- EE.VMULAS.S8.QACC.LD.IP.QUP qu, as, imm16, qx, qs0, qs1

**Description Section:**
This instruction divides registers qx and qy into 16 data segments by 8 bits. The signed multiplication result of the 16 sets of segments is added to the corresponding 20-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 20-bit signed number and then stored to the corresponding 20-bit data register in QACC_H and QACC_L.

During the operation, the lower 4 bits of the access address in register as are forced to be O, and then the 16-byte data is loaded from the memory to register qu. After the access is completed, the value in register as is incremented by a bit sign-extended constant in the instruction code segment left-shifted by 4.

At the same time, this instruction also obtains 16-byte unaligned data by concatenating and shifting the two registers qs0 and qs1 that store consecutive aligned data and stores it to qs0. The shift byte is stored in special register SAR_BYTE.

**Operation Section:**
- QACC_L[ 19: 0 ] = min(max(QACC_L[ 19: 0 ] + qx[ 7: 0 ] * qy[ 7: 0 ], -2^{19}), 2^{19}-1)
- QACC_L[ 39: 20 ] = min(max(QACC_L[ 39: 20 ] + qx[ 15: 8 ] * qy[ 15: 8 ], -2^{19}), 2^{19}-1)
- QACC_L[ 59: 40 ] = min(max(QACC_L[ 59: 40 ] + qx[ 23: 16 ] * qy[ 23: 16 ], -2^{19}), 2^{19}-1)
- QACC_L[ 79: 60 ] = min(max(QACC_L[ 79: 60 ] + qx[ 31: 24 ] * qy[ 31: 24 ], -2^{19}), 2^{19}-1)
- QACC_L[ 99: 80 ] = min(max(QACC_L[ 99: 80 ] + qx[ 39: 32 ] * qy[ 39: 32 ], -2^{19}), 2^{19}-1)
- QACC_L[119:100] = min(max(QACC_L[119:100] + qx[ 47: 40 ] * qy[ 47: 40 ], -2^{19}), 2^{19}-1)
- QACC_L[139:120] = min(max(QACC_L[139:120] + qx[ 55: 48 ] * qy[ 55: 48 ], -2^{19}), 2^{19}-1)
- QACC_L[159:140] = min(max(QACC_L[159:140] + qx[ 63: 56 ] * qy[ 63: 56 ], -2^{19}), 2^{19}-1)
- QACC_H[ 19: 0 ] = min(max(QACC_H[ 19: 0 ] + qx[ 71: 64 ] * qy[ 71: 64 ], -2^{19}), 2^{19}-1)
- QACC_H[ 39: 20 ] = min(max(QACC_H[ 39: 20 ] + qx[ 79: 72 ] * qy[ 79: 72 ], -2^{19}), 2^{19}-1)
- QACC_H[ 59: 40 ] = min(max(QACC_H[ 59: 40 ] + qx[ 87: 80 ] * qy[ 87: 80 ], -2^{19}), 2^{19}-1)
- QACC_H[ 79: 80 ] = min(max(QACC_H[ 79: 80 ] + qx[ 95: 88 ] * qy[ 95: 88 ], -2^{19}), 2^{19}-1)
- QACC_H[ 99: 100] = min(max(QACC_H[ 99: 100] + qx[103: 96 ] * qy[103: 96 ], -2^{19}), 2^{19}-1)
- QACC_H[119:120] = min(max(QACC_H[119:120] + qx[111:104 ] * qy[111:104 ], -2^{19}), 2^{19}-1)
- QACC_H[139:140] = min(max(QACC_H[139:140] + qx[139:112 ] * qy[139:112 ], -2^{19}), 2^{19}-1)

**Footer Information:**
Espressif Systems
Page number: 230
Document version information: ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback link