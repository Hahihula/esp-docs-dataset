**Title: Peripherals**

- **SPI0**: used by ESP32-S3’s GDMA controller and cache to access in-package or off-package flash/PSRAM

- **SPI1**: used by the CPU to access in-package or off-package flash/PSRAM

- **SPI2**: a general purpose SPI controller with access to a DMA channel allocated by the GDMA controller

- **SPI3**: is a general purpose SPI controller with access to a DMA channel allocated by the GDMA controller

**Feature List**

- **SPI0 and SPI1:**
  - Supports Single SPI, Dual SPI, Quad SPI, Octal SPI, QPI, and OPI modes
  - 8-line SPI mode supports single data rate (SDR) and double data rate (DDR)
  - Configurable clock frequency with a maximum of 120 MHz for 8-line SPI SDR/DDR modes
  - Data transmission is in bytes

- **SPI2:**
  - Supports operation as a master or slave
  - Connects to a DMA channel allocated by the GDMA controller
  - Supports Single SPI, Dual SPI, Quad SPI, Octal SPI, QPI, and OPI modes
  - Configurable clock polarity (CPOL) and phase (CPHA)
  - Configurable clock frequency
  - Data transmission is in bytes
  - Configurable read and write data bit order: most-significant bit (MSB) first, or least-significant bit (LSB) first

- **As a master**
  - Supports 2-line full-duplex communication with clock frequency up to 80 MHz
  - Full-duplex 8-line SPI mode supports single data rate (SDR) only
  - Supports 1-, 2-, 4-, 8-line half-duplex communication with clock frequency up to 80 MHz

- **As a slave**
  - Half-duplex 8-line SPI mode supports both single data rate (up to 80 MHz) and double data rate (up to 40 MHz)
  - Provides six SPI_CS pins for connection with six independent SPI slaves
  - Configurable CS setup time and hold time

- **SPI3:**
  - Supports operation as a master or slave