**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Register Information:**
- Register Name: SPI_CLOCK_REG (0x18)
- GoBack

**Bitfield Table:**

| Bit | Description |
|-----|-------------|
| 31 | - |
| ... | ... |
| 6 | - |
| 5 | - |
| 4 | - |
| 3 | - |
| 2 | SPI_CLKCONT_N |
| 1 | SPI_CLKCONT_H |
| 0 | SPI_CLKCONT_L |

**Text Descriptions:**

- **SPI_CLK_EQU_SYSCLK**: In master mode, when this bit is set to 1, SPI output clock is equal to system clock; when set to 0, SPI output clock is divided from system clock. In slave mode, it should be set to 0.
  
- **SPI_CLKDIV_PRE**: In master mode, it is used to configure the pre-divider value for SPI output clock. It is only valid when SPI_CLK_EQU_SYSCLK is 0. In slave mode, it should be set to 0.

- **SPI_CLKCNT_N**: In master mode, it is used to configure the divider for SPI output clock. It is only valid when SPI_CLK_EQU_SYSCLK is 0.
  
- **SPI_CLKCNT_H**: In master mode, `SPI_CLKCNT_H = [SPI_CLKCNT_N+1] / 2`. It is only valid when SPI_CLK_EQU_SYSCLK is 0.

- **SPI_CLKCNT_L**: In master mode, it is equal to SPI_CLKCNT_N. It is only valid when SPI_CLK_EQUSysclk is O.
  
**Footer:**
Espressif Systems
370 ESP32 TRM (Version 5.6)
Submit Documentation Feedback