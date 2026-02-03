**Chapter Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Number and Name:**
18.144 EE.VMULAS.S16.QACC.LDBC.INCP

**Instruction Word Table:**
- `100`
- `qu[2]`
- `0111`
- `qu[1]`
- `qy[2]`
- `qu[0]`
- `qy[1:0]`
- `qx[2:0]`
- `as[3:0]`
- `0100`

**Assembler Syntax:**
EE.VMULAS.S16.QACC.LDBC.INCP qu, as, qx, qy

**Description:**
This instruction divides registers qx and qy into 8 data segments by 16 bits. Then, the signed multiplication result of 8 sets of segments is added to the corresponding 40-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 40-bit signed number and then stored to the corresponding 40-bit data segment in QACC_H and QACC_L.

At the same time, this instruction forces the lower bit of the access address in register as to O, loads 16-bit data from memory, and broadcasts it to the eight 16-bit data segments in register qu. After the access, the value in register as is incremented by 2.

**Operation:**
```
QACC_L[39:0] = min(max(QACC_L[39:0] + qx[15:0] * qy[15:0], -2^39), QACC_L[79:40] = max(QACC_L[79:40] + qx[31:16] * qy[31:16], -2^39),
                   2^39-1)                 2^39-1)

QACC_L[119:80] = min(max(QACC_L[119:80] + qx[47:32] * qy[47:32], -2^39), QACC_L[159:120] = min(max(QACC_L[159:120] + qx[63:48] * qy[63:48], -2^39),
                   2^39-1)                 2^39-1)

QACC_H[39:0] = min(max(QACC_H[39:0] + qx[79:64] * qy[79:64], -2^39), QACC_H[79:40] = min(max(QACC_H[79:40] + qx[95:80] * qy[95:80], -2^39),
                   2^39-1)                 2^39-1)

QACC_H[119:80] = min(max(QACC_H[119:80] + qx[111:96] * qy[111:96], -2^39), QACC_H[159:120] = min(max(QACC_H[159:120] + qx[127:112] * qy[127:112], -2^39),
                   2^39-1)                 2^39-1)

qu[127:0] = {8(load16({as[31:1],1{0}}))
as[31:0] = as[31:0] + 2
```