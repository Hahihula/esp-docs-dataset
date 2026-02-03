**Title:**
Chapter 30 SPI Controller (SPI)

**Header:**
Register 30.14. SPI_CLK_GATE_REG (0x00E8)

**Binary Representation Table:**
- The table shows a binary representation with various bits labeled, such as "SPL_MST_CLK_SEL" and others.

**Body Text:**

- **SPI_CLK_EN**: Set this bit to enable clock gate. (R/W)
  
- **SPI_MST_CLK_ACTIVE**: Set this bit to power on the SPI module clock. (R/W)

- **SPI_MST_CLK_SEL**: This bit is used to select SPI module clock source in master mode.
  - `1: PLL_F80M_CLK`
  - `0: XTAL_CLK`

**Footer Information:**
Espressif Systems
Page number: 1165

**Document Version and Feedback Link:**
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback