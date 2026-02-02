**Title: Chapter 20 SPI Controller (SPI)**

---

### Figure Caption:
- **Figure 20.3-1:** SPI Master and Slave Full-duplex/Half-duplex Communication

---

**Body Text:**

The SPI1~SPI3 controllers can communicate with other slaves as a standard SPI master. SPI2 and SPI3 can be configured as either a master or slave. Every SPI master can be connected to three slaves at most by default. When not using DMA, the maximum length of data received/sent in one burst is 64 bytes. The data length is in multiples of one byte.

---

**Subsection:**
- **20.3.1 GP-SPI Four-line Full-duplex Communication**

When configured to four-line full-duplex mode, the ESP32 SPI can act as either a master or a slave. The length of received and sent data needs to be set by configuring the SPI_MISO_DLEN_REG, SPI_MOSI_DLEN_REG registers for master mode as well as SPI_SLV_RDBUF_DLEN_REG, SPI_SLV_WRBUF_DLEN_REG registers for slave mode. The SPI_DOUTDIN bit and SPI_USR_MOSI bit in register SPI_USER_REG should be configured to enable this communication mode. The SPI_USR bit in register SPI_CMD_REG needs to be configured to initialize a data transfer.

---

**Subsection:**
- **20.3.2 GP-SPI Four-line Half-duplex Communication**

When configured to four-line half-duplex mode, the ESP32 SPI can act as either a master or a slave. In this mode, the SPI communication supports flexible communication format as: command + address + dummy phase + received and/or sent data. The format is specified as follows:

1. **command:** length of 0~16 bits; Master Out Slave In (MOSI).
2. **address:** length of 0~32/64 bits; Master Out Slave In (MOSI).
3. **dummy phase:** length of 0~256 SPI clocks.
4. **received and/or sent data:** length of 0~512 bits (64 bytes); Master Out Slave In (MOSI) or Master In Slave Out (MISO).

The address length is up to 32 bits in GP-SPI master mode and 64 bits in QSPI master mode. The command phase, address phase, dummy phase and received/sent data phase are controlled by bits SPI_USR_COMMAND, SPI_USR_ADDR, SPI_USR_DUMMY, and SPI_USR_MOSI/SPI_USR_MOSI respectively in register SPI_USER_REG. A certain phase is enabled only when its corresponding control bit is set to 1. Details can be found in `register description`. When SPI works as a master, the register can be configured by software as required to determine whether or not to enable a certain phase.

When SPI works as a slave, the communication format must contain command, address, received and/or sent data, among which the command has several options listed in Table 20.3-1. During data transmission or reception:

---

**Footer:**
- **Espressif Systems**
- Page number: `356`
- Document version: `ESP32 TRM (Version 5.6)`
- Link to submit feedback: `[Submit Documentation Feedback](#)`