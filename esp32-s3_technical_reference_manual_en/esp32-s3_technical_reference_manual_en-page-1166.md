**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Header:**
Register 30.15. SPI_DIN_MODE_REG (0x0024NS)

**Binary Representation Table:**
- The table shows the binary representation of a register with various bits labeled, such as `SPL_TIMING HOLK_ACTIVE`, `SPL_DIN_MODE`, etc.

**Subsection Title and Description:**
SPI_DINO_MODE
Configure the input mode for input data bit0 signal. Can be configured in CONF state.
- **(R/W) Options:** 
  - O: input without delay
  - 1: input data is delayed by the falling edge of SPI_CLK for (SPI_DINO_NUM + 1) cycles

**Subsection Title and Description:**
SPI_DIN1_MODE
Configure the input mode for input data bit1 signal. Can be configured in CONF state.
- **(R/W) Options:** 
  - O: input without delay
  - 1: input data is delayed by the falling edge of SPI_CLK for (SPI_DIN1_NUM + 1) cycles

**Subsection Title and Description:**
SPI_DIN2_MODE
Configure the input mode for input data bit2 signal. Can be configured in CONF state.
- **(R/W) Options:** 
  - O: input without delay
  - 1: input data is delayed by the falling edge of SPI_CLK for (SPI_DIN2_NUM + 1) cycles

**Footer Note:**
Continued on the next page...

**Document Footer Information:**
Espressif Systems  
Page Number: 1166  
Document Version: ESP32-S3 TRM (Version 1.7)

**Navigation Links:**
Submit Documentation Feedback