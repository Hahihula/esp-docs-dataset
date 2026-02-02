**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Tables and Descriptions**

1. **Table 20.4-1. Clock Polarity and Phase, and Corresponding SPI Register Values for SPI Master**
   - Columns:
     - Registers
     - mode0
     - mode1
     - mode2
     - mode3

   | Registers                          | mode0 | mode1 | mode2 | mode3 |
   |-------------------------------------|-------|-------|-------|-------|
   | SPI_CK_IDLE_EDGE                    | 0     | 0     | 1     | 1     |
   | SPI_CK_OUT_EDGE                     | 0     | 1     | 1     | 0     |
   | SPI_MISO_DELAY_MODE                 |       |       |       |       |
   | SPI_MOSI_DELAY_NUM                  |       |       |       |       |
   | SPI_MOSI_DELAY_MODE                 |       |       |       |       |

2. **Table Description:**
   - The text explains that the SPI_MISO_DELAY_MODE[1:0] bit, SPI_MISO_DELAY_NUM[2:0] bit in register SPI_CTRL2_REG show clock polarity and phase as well as corresponding register values for ESP32 SPI master.
   - It notes differences between mode0 and mode2 configurations.

3. **Table 20.4-2. Clock Polarity and Phase, and Corresponding SPI Register Values for SPI Slave**
   - Columns:
     - Registers
     - Non-DMA | DMA

   | Registers                          | Non-DMA | DMA |
   |-------------------------------------|---------|-----|
   | SPI_CK_IDLE_EDGE                    | 1       | 0   |
   | SPI_CK_I_EDGE                       |         |     |
   | SPI_MISO_DELAY_MODE                 |         |     |
   | SPI_MOSI_DELAY_NUM                  |         |     |
   | SPI_MOSI_DELAY_MODE                 |         |     |

4. **Table Description:**
   - The text explains the meaning of mode0 and mode1 in terms of CPOL (Clock Polarity Low) values.
   - It describes how data changes on rising or falling edges.

**Footer Information:**
- Page number 359
- Company name: Espressif Systems
- Document version: ESP32 TRM (Version 5.6)
- Link to submit documentation feedback

**Navigation Links:**
- GoBack button at the top right corner