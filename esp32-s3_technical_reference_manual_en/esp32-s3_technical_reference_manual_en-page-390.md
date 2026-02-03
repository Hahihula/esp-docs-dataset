**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

**Section Header:**
GoBack

**Register Information for Register 3.23, GDMA_INIFO_STATUS_CHn_REG (n: 0-4) (0x0018+192*n):**

| Bit Position | Name                          |
|--------------|-------------------------------|
| 31           | reserved                      |
| 29           | reserved                      |
| 28           | GDMA_INIFO_N_T3_CHn          |
| 27           | reserved                      |
| 26           | reserved                      |
| 25           | reserved                      |
| 24           | reserve                       |
| 23           | reserve                       |
| 19           | reserve                       |
| 18           | GDMA_INIFO_N_T2_CHn          |
| 17           | reserved                      |
| 16           | reserved                      |
| 15           | reserved                      |
| 14           | reserved                      |
| 13           | GDMA_INIFO_N_T1_CHn          |
| 12           | reserve                       |
| 11           | reserve                       |
| 10           | GDMA_INIFO_N_T0_CHn          |
| 9            | reserve                       |
| 8            | reserved                      |
| 7            | reserved                      |
| 6            | GDMA_INIFO_EMPTY_L3_CHn      |
| 5            | GDMA_INIFO_FULL_L2_CHn       |
| 4            | GDMA_INIFO_EMPTY_L1_CHn      |
| 3            | GDMA_INIFO_FULL_L1_CHn       |
| 2            | GDMA_INIFO_EMPTY_L0_CHn      |
| 1            | GDMA_INIFO_FULL_L0_CHn       |
| 0            | Reset                         |

**Description of Bits:**
- **GDMA_INIFO_FULL_L1_CHn:** L1 RX FIFO full signal for RX channel O. (RO)
- **GDMA_INIFO_EMPTY_L1_CHn:** L1 RX FIFO empty signal for RX channel O. (RO)
- **GDMA_INIFO_FULL_L2_CHn:** L2 RX FIFO full signal for RX channel 0. (RO)
- **GDMA_INIFO_EMPTY_L2_CHn:** L2 RX FIFO empty signal for RX channel 0. (RO)
- **GDMA_INIFO_FULL_L3_CHn:** L3 RX FIFO full signal for RX channel O. (RO)
- **GDMA_INIFO_EMPTY_L3_CHn:** L3 RX FIFO empty signal for RX channel 0. (RO)
- **GDMA_INIFO_CNT_L1_CHn:** The register stores the byte number of the data in L1 RX FIFO for RX channel O. (RO)
- **GDMA_INIFO_CNT_L2_CHn:** The register stores the byte number of the data in L2 RX FIFO for RX channel 0. (RO)
- **GDMA_INIFO_CNT_L3_CHn:** The register stores the byte number of the data in L3 RX FIFO for RX channel O. (RO)

**Register Information for Register 3.24, GDMA_IN_STATE_CHn_REG (n: 0-4) (0x024+192*n):**

| Bit Position | Name                          |
|--------------|-------------------------------|
| 31           | reserved                      |
| 23           | reserve                       |
| 22           | reserve                       |
| 20           | GDMA_INLINK_DSCR_ADDR_CHn    |
| 19           | reserve                       |
| 18           | reserve                       |
| 17           | reserve                       |
| 16           | reserved                      |
| 15           | reserved                      |
| 14           | reserved                      |
| 13           | GDMA_INLINK_DSCR_ADDR_CHn    |
| 12           | reserve                       |
| 11           | reserve                       |
| 10           | reserve                       |
| 9            | reserve                       |
| 8            | reserve                       |
| 7            | reserved                      |
| 6            | GDMA_INLINK_DSCR_ADDR_CHn    |
| 5            | reserve                       |
| 4            | reserve                       |
| 3            | reserve                       |
| 2            | reserve                       |
| 1            | reserve                       |
| 0            | Reset                         |

**Description of Bits:**
- **GDMA_INLINK_DSCR_ADDR_CHn:** This register stores the lower 18 bits of the next receive descriptor address that is pre-read (but not processed yet). If the current receive descriptor is the last descriptor, then this field represents the address of the current receive descriptor. (RO)

**Footer:**
Espressif Systems
390 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback