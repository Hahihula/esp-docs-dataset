**Title:**
Chapter 1 Processor Instruction Extensions (PIE)

**Section Title:**
1.8.165 EE.VMULAS.U16.QACC.LD.IP.QUP

**Subsection Titles and Content:**

- **Instruction Word**: 
  - Description of the instruction word `0101 imm16[5:4] qu[2:1] qy[0] qs0[2:0] qu[0] qs1[2:0] qx[1:0] qx[2:1] imm16[3:0] as[3:0] 111 qx[2]`

- **Assembler Syntax**:
  - `EE.VMULAS.U16.QACC.LD.IP.QUP qu, as, imm16, qx, qs0, qs1`

- **Description**: 
  - This instruction divides registers qx and qy into 8 data segments by 16 bits. The unsigned multiplication result of the sets of segments is added to the corresponding 40-bit data segment in special registers QACC_H and QACC_L respectively. The calculated result is saturated to a 40-bit unsigned number and then stored to the corresponding 40-bit data register in QACC_H and QACC_L.
  - During operation, lower 4 bits of access address in register as are forced to be zero (0), followed by loading an 16-byte data from memory into register qu. After accessing is completed, value in register as incremented with a sign-extended constant instruction code segment left-shifted by four bit positions.
  - This operation also obtains the 16-byte unsigned data byte by concatenating and shifting consecutive aligned data stored to two registers qs0 and qs1.

- **Operation**:
  - Detailed operations involving various memory addresses, shifts, and arithmetic operations are listed in a step-by-step format. For example: 
    ```
    QACC_L[39:0] = min(QACC_L[39:0] + qx[15:0] * qy[15:0], 2^{40}-1)
    QACC_L[79:40] = min(QACC_L[79:40] + qx[31:16] * qy[31:16], 2^{40}-1)
    ...
    QACC_H[39:0] = min(QACC_H[39:0] + qx[79:64] * qy[63:48], 2^{40}-1)
    QACC_H[79:40] = min(QACC_H[79:40] + qx[95:80] * qy[95:80], 2^{40}-1)
    ...
    ```

**Footer**: 
- Page number and document version information:
  - "Espressif Systems ESP32-S3 TRM (Version 1.7)"
  - "Submit Documentation Feedback"