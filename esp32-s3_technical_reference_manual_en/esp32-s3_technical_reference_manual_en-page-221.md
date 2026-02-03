**Title: Chapter 1 Processor Instruction Extensions (PIE)**

**Section Title: 1.8.145 EE.VMULAS.S16.QACC.LDBC.INCP.QUP**

---

### Instruction Word:
- `11000`
- `qu[2:1]`: `qy[0]`
- `qsO[2:0]`: `qu[0]`
- `qsI[1:0]`: `lqs[2:0]`
- `qsX[1:0]`: `as[3:0]`
- `111`
- `qx[2]`

---

### Assembler Syntax
`EE.VMULAS.S16.QACC.LDBC.INCP.QUP qu, as, qx, qy, qsO, qsI`

---

### Description

This instruction divides registers `qx` and `qy` into 8 data segments by 16 bits. Then, the signed multiplication result of 8 sets of segments is added to the corresponding 40-bit data segment in special registers `QACC_H` and `QACC_L` respectively. The calculated result is saturated to a 40-bit signed number and then stored to the corresponding 40-bit data segment in `QACC_H` and `QACC_L`.

At the same time, this instruction forces the lower bit of the access address in register `as` to 0; loads 16-bit data from memory, and broadcasts it to the eight 16-bit data segments in register `qu`. After the access, the value in register `as` is incremented by 2.

At the same time, this instruction also obtains 16-byte unaligned data by concatenating and shifting consecutive aligned data stored in the two registers `qsO` and `qsI` and stores it to `qsO`. The shift byte is stored in special register `SAR_BYTE`.

---

### Operation

```
QACC_L[39:0] = min(max(QACC_L[39:0] + qx[15:0], 0) * qy[15:0], -2^{39}), 
               2^{39}-1)

QACC_L[79:40] = min(max(QACC_L[79:40] + qx[31:16], 0) * qy[31:16], -2^{39}),
                 2^{39}-1

QACC_L[119:80] = min(max(QACC_L[119:80] + qx[47:32], 0) * qy[47:32], -2^{39}),
                   2^{39}-1

QACC_L[159:120] = min(max(QACC_L[159:120] + qx[63:48], 0) * qy[63:48], -2^{39}),
                      2^{39}-1

QACC_H[39:0] = min(max(QACC_H[39:0] + qx[79:64], 0) * qy[79:64], -2^{39}), 
                   2^{39}-1

QACC_H[79:40] = min(max(QACC_H[79:40] + qx[95:80], 0) * qy[95:80], -2^{39}), 
                   2^{39}-1

QACC_H[119:80] = min(max(QACC_H[119:80] + qx[111:96], 0) * qy[111:96], -2^{39}), 
                     2^{39}-1

QACC_H[159:120] = min(max(QACC_H[159:120] + qx[127:112], 0) * qy[127:112], -2^{39}), 
                          2^{39}-1

qu[127:0] = {8{load16({as[31:1],1{0})}}}

as[31:0] = as[31:0] + 2

qsO[127:0] = {qsI[127:0], qsO[127:0]} >> {SAR_BYTE[3:0] << 3}
```

---

**Footer:**  
Espressif Systems  
Page number: **221**  
Document version and type information at the bottom.