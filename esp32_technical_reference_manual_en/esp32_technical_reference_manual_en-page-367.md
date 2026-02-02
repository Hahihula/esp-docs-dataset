**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Section Header:**
Register 20.3. SPI_CTRL_REG (0x8)

**Binary Diagram Description with Labels and Values for Each Bit:**
- The diagram shows a binary representation of the register, labeled from bits 31 to bit 0.
- Bits are marked as follows:
  - Reserved
  - SPI_WR_BIT_ORDER
  - SPI_RD_BIT_ORDER
  - SPI_FREAD_QIO
  - SPI_FREAD_DIO
  - SPI_WP
  - SPI_FREAD_QUAD
  - SPI_FREAD_DUAL
  - SPI_FASTRD_MODE

**Bit Descriptions:**
- **SPI_WR_BIT_ORDER:** This bit determines the bit order for command, address and data in transmitted signal. Values:
  - 1 sends LSB first; 
  - 0 sends MSB first.
  (R/W)
  
- **SPI_RD_BIT_ORDER:** This bit determines the bit order for received data in received signal. Values:
  - receives LSB first;
  - receives MSB first.
  (R/W)

- **SPI_FREAD_QIO:** This bit is used to enable four-line address writes and data reads in QSPI mode.
  (R/W)
  
- **SPI_FREAD_DIO:** This bit is used to enable two-line address writes and data reads in QSPI mode. 
  (R/W)
  
- **SPI_WP:** This bit determines the write-protection signal output when SPI is idle in QSPI mode:
  - Values: 
    - 1 outputs high;
    - 0 outputs low.
  (R/W)

- **SPI_FREAD_QUAD:** This bit used to enable four-line data reads in QSPI mode.  
  (R/W)
  
- **SPI_FREAD_DUAL:** This bit is used to enable two-line data reads in QSPI mode:
  (R/W)
  
- **SPI_FASTRD_MODE:** Reserved.

**Section Header:**
Register 20.4. SPI_CTRL1_REG (0xC)

**Binary Diagram Description with Labels and Values for Each Bit:**
- The diagram shows a binary representation of the register, labeled from bits 31 to bit 0.
- Bits are marked as follows:
  - Reserved
  - SPI_CS_HOLD_DELAY

**Bit Descriptions:**
- **SPI_CS_HOLD_DELAY:** Reserved.

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback  
ESP32 TRM (Version 5.6)