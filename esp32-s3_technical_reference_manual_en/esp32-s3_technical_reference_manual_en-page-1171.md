**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Header:**
Register 30.17. SPI_DOUT_MODE_REG (0x002C)

**Continuation Note:**
Continued from the previous page...

**Subsection with List and Description for SPI_DOUT6_MODE (for SPI2 only):**
- **Title:** SPI_DOUT6_MODE (for SPI2 only)
  - Configure the output mode for output data bit6 signal. Can be configured in CONF state. (R/W)
    - `0`: output without delay
    - `1`: output data is delayed by the falling edge of SPI_CLK for one cycle

**Subsection with List and Description for SPI_DOUT7_MODE (for SPI2 only):**
- **Title:** SPI_DOUT7_MODE (for SPI2 only)
  - Configure the output mode for output data bit7 signal. Can be configured in CONF state. (R/W)
    - `0`: output without delay
    - `1`: output data is delayed by the falling edge of SPI_CLK for one cycle

**Subsection with List and Description for SPI_D_DQS_MODE (for SPI2 only):**
- **Title:** SPI_D_DQS_MODE (for SPI2 only)
  - Configure the output mode for output SPI_DQS signal. Can be configured in CONF state. (R/W)
    - `0`: output without delay
    - `1`: output data is delayed by the falling edge of SPI_CLK for one cycle

**Footer:**
Espressif Systems  
Page number and document version information at bottom right corner:
ESP32-S3 TRM (Version 1.7)