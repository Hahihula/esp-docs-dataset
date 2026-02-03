**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Navigation Link:**
GoBack

**Register Information:**
- **Register Name:** Register 30.15, SPI_DIN_MODE_REG (0x0024)
- **Continuation Note:** Continued from the previous page...

**Section Title and Description:**
- **Title:** SPI_DIN7_MODE (for SPI2 only)
- **Description:** Configure the input mode for input data bit 7 signal. Can be configured in CONF state.

**List of Input Modes with Descriptions:**
1. `0`: input without delay
2. `1`: input data is delayed by the falling edge of SPI_CLK for (SPI_DIN7_NUM +1) cycles.
3. `2`: input data is delayed by the rising edge of clk_hclk for (SPI_DIN7_NUM +1) cycles, and then delayed by the rising edge of SPI_CLK for one cycle
4. `3`: input data is delayed by the rising edge of clk_hclk for (SPI_DIN7_NUM +1) cycles, and then delayed by the falling edge of SPI_CLK for one cycle

**Additional Register Information:**
- **Register Name:** SPI_TIMING_HCLK_ACTIVE
- **Values Description:**
  - `0`: disable clk_hclk. Can be configured in CONF state.
  - `1`: Enable clk_hclk (high-frequency clock) in SPI input timing module.

**Footer Information:**
- Company Logo and Text: Espressif Systems
- Document Version Number: ESP32-S3 TRM (Version 1.7)
- Page Number: 1168

**Action Link at the Bottom of the Page:** Submit Documentation Feedback