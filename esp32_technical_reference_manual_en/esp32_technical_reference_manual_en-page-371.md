**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Register Information:**
- Register Name: SPI_USER_REG (0x1C)
- GoBack button

**Bit Description Table:**

| Bit Number | Bit Name                          |
|------------|-----------------------------------|
| 31         | SPI_USER_COMMAND                  |
| 30         | SPI_USER_ADDR                     |
| 29         | SPI_USER_DUMMY                    |
| 28         | SPI_USER_MISO                      |
| 27         | SPI_USER_MOSI                      |
| 26         | SPI_USER_MISO_HIGHPART             |
| 25         | SPI_USER_MISO_LOWPART              |
| 24         | SPI_USER_IDLE                      |
| ...        | ...                               |
| 1           | SPI_CS_HOLD                        |

**Bit Description:**

- **SPI_USR_COMMAND:** This bit enables the command phase of an SPI operation in SPI half-duplex mode and QSPI mode. (R/W)
  
- **SPI_USR_ADDR:** This bit enables the address phase of an SPI operation in SPI half-duplex mode and QSPI mode. (R/W)

- **SPI_USR_DUMMY:** This bit enables the dummy phase of an SPI operation in SPI half-duplex mode and QSPI mode. (R/W)

- **SPI_USR_MISO:** This bit enables the read-data phase of an SPI operation in SPI half-duplex mode and QSPI mode. (R/W)

- **SPI_USR_MOSI:** This bit enables the write-data phase of an SPI operation in SPI half-duplex mode and QSPI mode. (R/W)

- **SPI_USR_DUMMY_IDLE:** The SPI clock signal is disabled in the dummy phase when the bit is set in SPI half-duplex mode and QSPI mode. (R/W)

- **SPI_USR_MOSI_HIGHPART:** If set, MOSI data is stored in SPI_W8 ~ SPI_W15 of the SPI buffer.
  
- **SPI_USR_MISO_HIGHPART:** If set, MISO data is stored in SPI_W8 ~ SPI_W15 of the SPI buffer.

- **SPI_SIO:** Set this bit to enable three-line half-duplex communication. (R/W)

- **SPI_FWRITE_QIO:** Reserved.
  
- **SPI_FWRITE_DIO:** Reserved.
  
- **SPI_FWRITE_QUAD:** Reserved.
  
- **SPI_FWRITE_DUAL:** Reserved.

- **SPI_WR_BYTE_ORDER:** This bit determines the byte order of the command, address and data in transmitted signal. 1: big-endian; O: little-endian. (R/W)

- **SPI_RD_BYTE_ORDER:** This bit determines the byte order of received data in transmitted signal. 1: big-endian; 0: little_endian. (R/W)

- **SPI_CK_OUT_EDGE:** This bit, combined with SPI_MOSI_DELAY_MODE, sets the MOSI signal delay mode. It is only valid in master mode. (R/W)

- **SPI_CK_IN_EDGE:** In slave mode, the bit is the same as SPI_CK_OUT_EDGE in master mode. It is combined with SPI_MISO_DELAY_MODE. It is only valid in slave mode.

**Footer:**
Continued on the next page...
Page number 371
ESP32 TRM (Version 5.6)
Submit Documentation Feedback