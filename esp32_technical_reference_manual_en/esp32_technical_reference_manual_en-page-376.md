**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Section Header:**
Register 20.15. SPI_SLAVE_REG (0x38)

**Body Text with Descriptions and Details for Each Register Field:**

- **SPI_SLV_WRBufDone**: The raw interrupt status bit for the `SPI_SLV_WRBuf_INT` interrupt.
  - It is set by hardware and cleared by software, only applicable to slave half-duplex mode. (R/W)

- **SPI_SLV_RdBufDone**: The raw interrupt status bit for the `SPI_SLV_RDBuf_INT`.
  - It is set by hardware and cleared by software, also applies to slave half-duplex mode.
  - (R/W)

**Register 20.16: SPI_SLAVE1_REG (0x3C)**

- **SPI_SVLSTATUS_BITLEN**: Only used in slave half-duplex mode; it configures the length of master writing into the status register.

- **SPI_SVLSTATUS_FAST_EN**: Reserved.
  
- **SPI_SVLSTATUS_READBACK**: Reserved.

- **SPI_SVL_RD_ADDR_BITLEN**: Indicates address length for a slave-read operation, valid only in slave half-duplex mode. (R/W)

- **SPI_SVL_WR_ADDR_BITLEN**: Indicates the same as above but applies to write operations.
  
- **SPI_SVL_WRSR DummyEN**: In slave mode; enables dummy phase during write-status operations and is applicable for read-status ops too.

- **SPI_SVL_RDSTADummyEN** & **SPI_SVL_WRBUFFDummyEN**: Enable the dummy phases in respective buffer operations, valid only when half-duplex.
  
- **SPI_SVL_RDBUFDummyEN**: Similar to above but applies during reading from buffers. 

**Footer Information:** 
Espressif Systems
376 ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Navigation Link:**
GoBack