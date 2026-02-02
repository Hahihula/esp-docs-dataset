**Chapter Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Section Header with Navigation Link:**
TWAI_ERR_CODE_CAP_REG.

**Table Description and Reference to Figure:**
Table 25.5-13 illustrates the bit fields of the TWAI_ERR_CODE_CAP_REG whilst Figure 25.5-5 illustrates the bit positions of a TWAI message.
- **Table Title:** Table 25.5-13. Bit Information of TWAI_ARB LOST_CAP_REG; TWAI Address 0x2c
- The table shows:
  - Bits: Bit 31-5, Bit 4, Bit 3, Bit 2, Bit 1, Bit 0.
  - Reserved and BITNO.4¹ for the first row with references to Table 25.5-13 notes (BITNO.3¹, BITNO.2¹).
  - BITNO.1¹ in second column followed by BITNO.0¹.

**Notes:**
- BITNO: Bit Number (BITNO) indicates the nth bit of a TWAI message where arbitration was lost.
- Extended frame messages are indicated with bits labeled from bit0 to bit31, showing identifiers and positions for SOF, Identifier, SRTR, IDE, RTR in different columns.

**Figure Reference:**
Figure 25.5-5. Positions of Arbitration Lost Bits

**Subsection Title:**
25.6 Register Summary

**Body Text with Explanation Note:**
The addresses in this section are relative to the TWAI base address provided in Table 3.3-6 in Chapter 3 System and Memory.
The abbreviations given in Column Access are explained in Section Access Types for Registers.

**Table of Configuration Registers (with columns Name, Description, Address, Access):**

| Name                   | Description                          | Address                | Access |
|------------------------|--------------------------------------|------------------------|--------|
| TWAI_MODE_REG         | Mode Register                        | 0x3FF6B000            | R/W     |
| TWAI_BUS_TIMING_0_REG | Bus Timing Register 0                | 0x3FF6B018            | RO / RW |
| TWAI_BUS_TIMING_1_REG | Bus Timing Register 1                | 0x3FF6B01C            | RO / RW |
| TWAI_ERR_WARNING_LIM_REG | Error Warning Limit Register         | 0x3FF6B034            | R/O     |
| TWAI_DATA_0_REG       | Data Register 0                      | 0x3FF6B040            | WO / RW |
| ...                    | ...                                  | ...                    | ...    |

**Footer:**
Espressif Systems
549 ESP32 TRM (Version 5.6)
Submit Documentation Feedback