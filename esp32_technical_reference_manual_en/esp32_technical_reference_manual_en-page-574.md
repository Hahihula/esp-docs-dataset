**Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**Menu:**
GoBack

**Register Information:**
- **Register Name:** SLCOINT_RAW_REG (0x4)
- **Description:** The raw interrupt bit for various operations in the slave controller.

**Interrupt Bits Description Table:**

| Bit Number | Offset | Description                                                                                   |
|------------|--------|------------------------------------------------------------------------------------------------|
| 31         | 0      | Reserved                                                                                        |
| ...        | ...    | ...                                                                                            |
| 2          | 7      | The interrupt mark bit for Host to interrupt Slave. (RO)                                      |
|            |        | ...                                            |

**Interrupt Bits:**
- **SLCOINT_SLCO_RX_DSCR_ERR_INT_RAW:** The raw interrupt bit for Slave sending descriptor error.
- **SLCOINT_SLCO_TX_DSCR_ERR_INT_RAW:** The raw interrupt bit for Slave receiving descriptor error.
- **SLCOINT_SLCO_RX_EOF_INT_RAW:** The interrupt mark bit for Slave sending operation finished. (RO)
- **SLCOINT_SLCO_RX_DONE_INT_RAW:** The raw interrupt bit to mark single buffer as sent by Slave. (RO)
- **SLCOINT_SLCO_TX_SUC_EOF_INT_RAW:** The raw interrupt bit to mark Slave receiving operation as finished. (RO)
- **SLCOINT_SLCO_TXDone_INT_RAW:** The raw interrupt bit to mark a single buffer as finished during Slave receiving operation. (RO)
- **SLCOINT_SLCO_TX_OVF_INT_RAW:** The raw interrupt bit to mark Slave receiving buffer overflow. (RO)
- **SLCOINT_SLCO_RX_UDF_INT_RAW:** The raw interrupt bit for Slave sending buffer underflow. (RO)
- **SLCOINT_SLCO_TX_START_INT_RAW:** The raw interrupt bit for registering Slave receiving initialization interrupt. (RO)
- **SLCOINT_SLCO_RX_START_INT_RAW:** The raw interrupt bit to mark Slave sending initialization interrupt. (RO)

**Host Interrupt Bits:**
- **SLCOINT_SLC_FRHOST_BIT7_INT_RAW, SLCOINT_SLC_FRHOST_BIT6_INT_RAW,..., SLCOINT_SLC_FRHOST_BIT0_INT_RAW:** Various interrupt marks for host-to-interrupt slave operations.

**Footer Information:**
Espressif Systems
574 ESP32 TRM (Version 5.6)
Submit Documentation Feedback