**Title: Chapter 20 SPI Controller (SPI)**

**Subtitle: Register 20.15. SPI_SLALE_REG (0x38)**

**Binary Diagram**
- The diagram shows a binary representation of the register with labels for each bit.

**Text Description and Table**

| Bit Number | Name                          |
|------------|-------------------------------|
| 31         | SPI_SYNC_RESET               |
| 30         | SPI_SLALE_MODE                |
| 29         | SPI_SLALE_WR_RD_BUF_EN       |
| 28         | SPI_SLALE_WR_RD_STA_EN       |
| 27         | SPI_SLALE_CMD DEFINE          |
| 26         | SPI_TRANS_CNT                 |
| 25         | SPI_SLALE_LAST_STATE          |
| 24         | SPI_SLALELast_COMMAND        |
| 23-18      | Reserved                      |
| 17         | SPI_CS_I_MODE                 |
| 16         | SPITrans_INTEN                |
| 15         | SPI_SLALE_WR_STA_INTEN       |
| 14         | SPI_SLALE_RD_STA_INTEN       |
| 13-0        | Reserved                      |

**Description of Register Bits:**

- **SPI_SYNC_RESET**: When set, it resets the latched values of the SPI clock line, CS line and data line. (R/W)
  
- **SPI_SLAVE_MODE**: This bit is used to set the mode of the SPI device. (R/W) 
  - `1`: slave mode;
  - `0`: master mode.

- **SPI_SLALE_WR_RD_BUF_EN**:
  - This bit is only used in slave half-duplex mode, where when it is set, the write and read data commands are enabled. (R/W)

- **SPI_SLALE_WR_RD_STA_EN**: 
  - This bit is only used in slave half-duplex mode, where when it is set, the write and read status commands are enabled. (R/W)

- **SPI_SLALE_CMD DEFINE**:
  - Reserved.

- **SPI_TRANS_CNT**: The counter for operations in both the master mode and the slave mode. (RO)

- **SPI_SLALELast_STATE**:
  - In slave mode, this contains the state of the SPI state machine. (RO)

- **SPI_SLALELast_COMMAND**:
  - Reserved.

- **SPI_CS_I_MODE**: Reserved.

- **SPITrans_INTEN**: The interrupt enable bit for the `SPI_TRANS_DONE_INT` interrupt. (R/W)

- **SPI_SLALE_WR_STA_INTEN**, **SPI_SLALE_RD_STA_INTEN**, and **SPI_SLALE_WRBuf_INTEN**:
  - These are the interrupt enable bits, applicable to specific SPI events.

- **SPITransDone**: The raw interrupt status bit for `SPI_TRANS_DONE_INT` interrupt. It is set by hardware and cleared by software. (R/W)

- **SPI_SLALE_WR_STA_INT**, **SPI_SLALE_RD_STA_INT**:
  - These are the raw interrupt status bits, applicable to specific SPI events.

**Footer:**
Continued on the next page...

**Company Information:** 
Espressif Systems

**Document Version and Feedback Link:**
ESP32 TRM (Version 5.6)
Submit Documentation Feedback