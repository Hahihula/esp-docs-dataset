**Title: Peripherals**

- **Connects to a DMA channel allocated by the GDMA controller**
- Supports Single SPI, Dual SPI, Quad SPI, and QPI modes

- Configurable clock polarity (CPOL) and phase (CPHA)

- Configurable clock frequency

- Data transmission is in bytes

- Configurable read and write data bit order: most-significant bit (MSB) first, or least-significant bit (LSB) first

**As a master**
  - Supports 2-line full-duplex communication with clock frequency up to 80 MHz
  - Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 80 MHz
  - Provides three SPI_CS pins for connection with three independent SPI slaves

- Configurable CS setup time and hold time

**As a slave**
  - Supports 2-line full-duplex communication with clock frequency up to 60 MHz
  - Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 60 MHz

For details, see [ESP32-S3 Technical Reference Manual > Chapter SPI Controller](#).

**Pin Assignment**

Note:
Please refer to ESP32-S3 Series Datasheet > Section IO MUX Function > Table IO MUX Pin Functions for the corresponding SPI interface details.

- **SPI0/1**
  - Via IO MUX:
    - Interface 4a is multiplexed with GPIO26 ~ GPIO32 via IO MUX. When used in conjunction with 4b, it can operate as the lower 4 bits data line interface and the CLK, CSO, and CS1 interfaces in 8-line SPI mode.
    - Interface 4b is multiplexed with GPIO33 ~ GPIO37 and SPI interfaces 4e and 4f via IO MUX. When used in conjunction with 4a, it can operate as the higher 4 bits data line interface and DQS interface in 8-line SPI mode.
    - Interface 4d is multiplexed with GPIO8 ~ GPIO14, RTC_GPIO8 ~ RTC_GPIO14, Touch Sensor interface, SAR ADC interface, and SPI interfaces 4c and 4g via IO MUX. Note that the fast SPI2 interface will not be available.

- **SPI2**
  - Via GPIO Matrix: The pins used can be chosen from any GPIOs via the GPIO Matrix.
  
**Footer**: 
Espressif Systems
Submit Documentation Feedback

ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6