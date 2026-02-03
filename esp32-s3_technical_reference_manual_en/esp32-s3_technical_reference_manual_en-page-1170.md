**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Header:**
Register 30.17. SPI_DOUT_MODE_REG (0x002C)

**Hexadecimal Memory Map Diagram Description:**
A diagram showing the memory map with addresses and corresponding registers, including:
- `0` to `9`
- `Reset` at address `0`

**Table of Registers:**

| Register Name | Description |
|---------------|-------------|
| **SPI_DOUT_MODE** | Configure the output mode for output data bit 0 signal. Can be configured in CONF state. (R/W) |
   - `0`: output without delay
   - `1`: output data is delayed by the falling edge of SPI_CLK for one cycle |
| **SPI_DOUT1_MODE** | Configure the output mode for output data bit1 signal. Can be configured in CONF state. (R/W) |
   - `0`: output without delay
   - `1`: output data is delayed by the falling edge of SPI_CLK for one cycle |
| **SPI_DOUT2_MODE** | Configure the output mode for output data bit2 signal. Can be configured in CONF state. (R/W) |
   - `0`: output without delay
   - `1`: output data is delayed by the falling edge of SPI_CLK for one cycle |
| **SPI_DOUT3_MODE** | Configure the output mode for output data bit3 signal. Can be configured in CONF state. (R/W) |
   - `0`: output without delay
   - `1`: output data is delayed by the falling edge of SPI_CLK for one cycle |
| **SPI_DOUT4_MODE (for SPI2 only)** | Configure the output mode for output data bit4 signal. Can be configured in CONF state. (R/W) |
   - `0`: output without delay
   - `1`: output data is delayed by the falling edge of SPI_CLK for one cycle |
| **SPI_DOUT5_MODE (for SPI2 only)** | Configure the output mode for output data bit5 signal. Can be configured in CONF state. (R/W) |
   - `0`: output without delay
   - `1`: output data is delayed by the falling edge of SPI_CLK for one cycle |

**Footer:**
Continued on the next page...

**Document Footer Information:**
Espressif Systems  
Page number 17/2, Document version ESP32-S3 TRM (Version 1.7)  

**Navigation Links:**
- Submit Documentation Feedback