**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Section Header:**
Register 20.17. SPI_SLAVE2_REG (0x40)

**Diagram Description with Labels and Values:**
- SPI_SLV_WRBUF_DUMMY_CYCLELEN
- SPI_SLV_RDBUF_DUMMY_CYCLELEN
- SPI_SLV_WRSTA_DUMMY_CYCLELEN

**Text Content under Diagrams:**

- **SPI_SLV_WRBUF_DUMMY_CYCLELEN**: It indicates the number of SPI clock cycles minus one for the dummy phase for write-data operations. It is only valid when SPI_SLV_WRBUF_DUMMY_EN is set to 1 in slave half-duplex mode (R/W).

- **SPI_SLV_RDBUF_DUMMY_CYCLELEN**: It indicates the number of SPI clock cycles minus one for the dummy phase for read-data operations. It is only valid when SPI_SLV_RDBUF_DUMMY_EN is set to 1 in slave half-duplex mode (R/W).

- **SPI_SLV_WRSTA_DUMMY_CYCLELEN**: It indicates the number of SPI clock cycles minus one for the dummy phase for write-status register operations. It is only valid when SPI_SLV_WRSTA_DUMMY_EN is set to 1 in slave half-duplex mode (R/W).

- **SPI_SLV_RDSTA_DUMMY_CYCLELEN**: It indicates the number of SPI clock cycles minus one for the dummy phase for read-status register operations. It is only valid when SPI_SLV_RDSTA_DUMMY_EN is set to 1 in slave half-duplex mode (R/W).

**Section Header:**
Register 20.18. SPI_SLAVE3_REG (0x44)

**Diagram Description with Labels and Values:**

- SPI_SLV_WRSTA_CMD_VALUE
- SPI_SLV_RDBUF_CMD_VALUE

**Text Content under Diagrams:**

- **SPI_SLV_WRSTA_CMD_VALUE**: Reserved.

- **SPI_SLV_RDSTA_CMD_VALUE**: Reserved.

- **SPI_SLV_WRBUF_CMD_VALUE**: Reserved. 

**Footer Information:**
Espressif Systems
377 ESP32 TRM (Version 5.6)
Submit Documentation Feedback