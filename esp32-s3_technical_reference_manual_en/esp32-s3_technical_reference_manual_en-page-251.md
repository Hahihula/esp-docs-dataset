**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.169 EE.VMULAS.U16.QACC.LDBC.INCP.QUP

**Subsection Titles and Content:**

- **Instruction Word**: 
  - `11000 qu[2:1] qy[0] qs0[2:0] qu[0] qs1[2:0] qx[1:0] qs0[2:0] as[3:0] 111 qx[2]`

- **Assembler Syntax**:
  - `EE.VMULAS.U16.QACC.LDBC.INCP.QUP qu, as, qx, qy, qs0, qs1`

- **Description**: 
  This instruction divides registers qx and qy into 8 data segments by 16 bits. Then, the unsigned multiplication result of the 8 sets of segments is added to the corresponding 40-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 40-bit unsigned number and then stored to the corresponding 40-bit data segment in QACC_H and QACC_L.
  
  At the same time, this instruction forces the lower 1 bit of the access address in register as to O, loads 16-bit data from memory, and broadcasts it to the eight 16-bit data segments in register qu. After the access, the value in register as is incremented by 2.
  
  At the same time, this instruction also obtains 16-byte unaligned data by concatenating and shifting consecutive aligned data stored in the two registers qs0 and qs1 and stores it to qs0. The shift byte is stored in special register SAR_BYTE.

- **Operation**:
  - `QACC_L[39:0] = min(QACC_L[39:0] + qx[15:0] * qy[15:0], 2^{40}-1)`
  - `QACC_L[79:40] = min(QACC_L[79:40] + qx[31:16] * qy[31:16], 2^{40}-1)`
  - ...
  - `QACC_L[159:120] = min(QACC_L[159:120] + qx[63:48] * qy[63:48], 2^{40}-1)`
  - `QACC_H[39:0] = min(QACC_H[39:0] + qx[79:64] * qy[79:64], 2^{40}-1)`
  - `QACC_H[79:40] = min(QACC_H[79:40] + qx[95:80] * qy[95:80], 2^{40}-1)`
  - ...
  - `QACC_H[159:120] = min(QACC_H[159:120] + qx[127:112] * qy[127:112], 2^{40}-1)`
  
  ```
  qu[127:0] = {8<load16(as[31:1],1{0})>
  as[31:0] = as[31:0] + 2
  qs0[127:0] = {qs1[127:0], qs0[127:0] >> 3}
  ```

**Footer**: 
- "Espressif Systems"
- Page number and document version information:
  - `251 ESP32-S3 TRM (Version 1.7)`
- Link to submit documentation feedback.

(Note: The text in the code block is formatted as it appears, with syntax highlighting for clarity.)