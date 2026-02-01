**Title: Functional Description**

**Subtitle: Serial Peripheral Interface (SPI)**

ESP32-S3 has the following SPI interfaces:

- **SPI0**: used by ESP32-S3’s GDMA controller and cache to access in-package or off-package flash/PSRAM.
  
- **SPI1**: used by the CPU to access in-package or off-package flash/PSRAM.

- **SPI2**: is a general purpose SPI controller with access to a DMA channel allocated by the GDMA controller.

- **SPI3**: is a general purpose SPI controller with access to a DMA channel allocated by the GDMA controller.

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
  
- As a slave:
  - Full-duplex and half-duplex SPI mode supports single data rate (SDR) only
  - Provides six SPI_CS pins for connection with six independent SPI slaves

**Additional Information:**
- Configurable CS setup time and hold time.

**Footer:** 
Espressif Systems  
Submit Documentation Feedback  
ESP32-S3 Series Datasheet v2.1