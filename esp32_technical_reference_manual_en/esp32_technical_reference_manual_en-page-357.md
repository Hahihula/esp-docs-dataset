**Title: Chapter 20 SPI Controller (SPI)**

---

**Table Title:** Table 20.3-1. Command Definitions Supported by GP-SPI Slave in Half-duplex Mode

| Command | Description |
|---------|-------------|
| 0x1     | Received by slave; writes data sent by the master into the slave status register via MOSI. |
| 0x2     | Received by slave; writes data sent by the master into the slave data buffer via MOSI. |
| 0x3     | Sent by slave; sends data in the slave buffer to master via MISO. |
| 0x4     | Sent by slave; sends data in the slave status register to master via MISO. |
| 0x6     | Writes master Data on MOSI into data buffer and then sends the date in the slave data buffer to MISO. |

**Body Text:**

The master can write the slave status register SPI_SLV_WR_STATUS_REG, and decide whether to read data from register SPI_SLV_WR_STATUS_REG or register SPI_RD_STATUS_REG via the SPI_SLV_STATUS_READBACK bit in register SPI_SLAVE_REG.

The SPI master can maintain communication with the slave by reading and writing slave status register, thus realizing complex communication with ease. 

The length of received and sent data is controlled by SPI_MISO_DLEN_REG and SPI_MOSI_DLEN_REG in master mode, as well as SPI_SLV_RDBUF_DLEN_REG and SPI_SLV_WRBUF_DLEN_REG in slave mode.

A reception or transmission of data is controlled by bit SPI_USR_MOSI or SPI_USR_MISO in SPI_USER_REG. The SPI_USR bit in register SPI_CMD_REG needs to be configured to initialize a data transfer.

---

**Subtitle:** 20.3.3 GP-SPI Three-line Half-duplex Communication

**Body Text:**

The three-line half-duplex communication differs from four-line half-duplex communication in that the reception and transmission shares one signal bus and that the communication format must contain command, address, received and/or sent data.

Software can enable three-line half-duplex communication by configuring SPI_SIO bit in SPI_USER_REG register. 

**Note:**

- In half-duplex communication, the order of command, address, received and/or sent data in the communication format should be followed strictly.
- In half-duplex communication, communication formats "command + address + received data + sent data" are not applicable to DMA.

When ESP32 SPI acts as a slave, the master CS should be active at least one SPI clock period before a read/write process is initiated, and should be inactive at least one SPI clock period after the read/write process is completed. 

---

**Footer:**

Espressif Systems  
ESP32 TRM (Version 5.6)  
Submit Documentation Feedback