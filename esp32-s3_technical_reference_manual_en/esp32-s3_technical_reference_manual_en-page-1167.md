**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Header:**
Register 30.15. SPI_DIN_MODE_REG (0x0024)

**Continuation Note:**
Continued from the previous page...

**Subsection Title and Description:**
SPI_DIN3_MODE
Configure the input mode for input data bit3 signal. Can be configured in CONF state. (R/W)
- 0: input without delay
- 1: input data is delayed by the falling edge of SPI_CLK for (SPI_DIN3_NUM +1) cycles
- 2: input data is delayed by the rising edge of clk_hclk for (SPI_DIN3_NUM +1) cycles, and then delayed by the rising edge of SPI_CLK for one cycle
- 3: input data is delayed by the rising edge of clk_hclk for (SPI_DIN3_NUM +1) cycles, and then delayed by the falling edge of SPI_CLK for one cycle

**Subsection Title with Restriction Note:**
SPI_DIN4_MODE (for SPI2 only)
Configure the input mode for input data bit4 signal. Can be configured in CONF state.
- 0: input without delay
- 1: input data is delayed by the falling edge of SPI_CLK for (SPI_DIN4_NUM +1) cycles
- 2: input data is delayed by the rising edge of clk_hclk for (SPI_DIN4_NUM +1) cycles, and then delayed by the rising edge of SPI_CLK for one cycle
- 3: input data is delayed by the rising edge of clk_hclk for (SPI_DIN4_NUM +1) cycles, and then delayed by the falling edge of SPI_CLK for one cycle

**Subsection Title with Restriction Note:**
SPI_DIN5_MODE (for SPI2 only)
Configure the input mode for input data bit5 signal. Can be configured in CONF state.
- 0: input without delay
- 1: input data is delayed by the falling edge of SPI_CLK for (SPI_DIN5_NUM +1) cycles
- 2: input data is delayed by the rising edge of clk_hclk for (SPI_DIN5_NUM +1) cycles, and then delayed by the rising edge of SPI_CLK for one cycle
- 3: input data is delayed by the rising edge of clk_hclk for (SPI_DIN5_NUM +1) cycles, and then delayed by the falling edge of SPI_CLK for one cycle

**Subsection Title with Restriction Note:**
SPI_DIN6_MODE (for SPI2 only)
Configure the input mode for input data bit6 signal. Can be configured in CONF state.
- 0: input without delay
- 1: input data is delayed by the falling edge of SPI_CLK for (SPI_DIN6_NUM +1) cycles
- 2: input data is delayed by the rising edge of clk_hclk for (SPI_DIN6_NUM +1) cycles, and then delayed by the rising edge of SPI_CLK for one cycle
- 3: input data is delayed by the rising edge of clk_hclk for (SPI_DIN6_NUM +1) cycles, and then delayed by the falling edge of SPI_CLK for one cycle

**Footer Note:**
Continued on the next page...

**Document Information:**
Espressif Systems  
ESP32-S3 TRM (Version 1.7)

**Navigation Link:**
GoBack