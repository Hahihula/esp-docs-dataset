**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Navigation Link:**
GoBack

**Section Header:**
Register 30.6. SPI_CTRL_REG (0x0008)

**Continuation Note:**
Continued from the previous page...

**Field Descriptions and Values with Explanation for Each Field in Register 30.6, SPI_CTRL_REG (0x0008):**

1. **SPI_HOLD_POL**
   - Description: This bit is used to set SPI_HOLD output value when SPI is in idle.
   - Options:
     - `0`: Output low
     - `1`: Output high

2. **SPI_WP_PUL**
   - Description: This bit is used to set the output value of write-protect signal when SPI is in idle.
   - Options:
     - `0`: Output low (Can be configured in CONF state)
     - `1`: Output high
     - Note: Can also be configured in CONF state

3. **SPI_RD_BIT_ORDER**
   - Description: In read-data (MISO) state, 1: LSB first; 0: MSB first.
   - Can be configured in CONF state.

4. **SPI_WR_BIT_ORDER**
   - Description:
     - In command (CMD), address (ADDR), and write-data (MOSI) states,
       - `0`: MSB first
       - `1`: LSB first

5. **Register 30.7, SPI_MS_DLEN_REG (0x001C)**

**Field Description for Register 30.7:**

- **SPI_MS_DATA_BITLEN**
   - Value Explanation:
     - The value of this field is the configured SPI transmission data bit length in master mode DMA-controlled transfer or CPU-controlled transfer.
     - Also, it represents the configured bit length in slave mode DMA RX controlled transfer.

**Bit Length Configuration Note for Register 30.7:**

- The register value shall be (expected bit number - 1).
- Can also be configured in CONF state
- Options:
  - `R/W`

**Footer Information:**
Espressif Systems

**Document Version and Link:**
ESP32-S3 TRM (Version 1.7)

**Link for Submitting Documentation Feedback:** 
Submit Documentation Feedback