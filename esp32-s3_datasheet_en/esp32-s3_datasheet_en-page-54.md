**Title: Functional Description**

- **SPI3**
  - Supports operation as a master or slave
  - Connects to a DMA channel allocated by the GDMA controller
  - Supports Single SPI, Dual SPI, Quad SPI, and QPI modes
    - Configurable clock polarity (CPOL) and phase (CPHA)
    - Configurable clock frequency
    - Data transmission is in bytes
    - Configurable read and write data bit order: most-significant bit (MSB) first, or least-significant bit (LSB) first
  - As a master:
    * Supports 2-line full-duplex communication with clock frequency up to 80 MHz
      - Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 80 MHz
    * Provides three SPI_CS pins for connection with three independent SPI slaves
  - Configurable CS setup time and hold time

- **As a slave**
  - Supports 2-line full-duplex communication with clock frequency up to 60 MHz
  - Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 60 MHz

For details, see [ESP32-S3 Technical Reference Manual > Chapter SPI Controller](#).

**Subtitle: Pin Assignment**

For details, see Section **2.3.5 Peripheral Pin Assignment**.

**Title: Two-Wire Automotive Interface (TWAI®)**

The TWI-Auto Automotive Interface is a multi-master, multi-cast communication protocol with error detection and signaling as well as inbuilt message priorities and arbitration.

**Subtitle: Feature List**

- Compatible with ISO 11898-1 protocol (CAN Specification 2.0)
- Standard frame format (11-bit ID) and extended frame format (29-bit ID)
- Bit rates from 1 Kbit/s to 1 Mbit/s
- Multiple modes of operation:
  - Normal
  - Listen Only
  - Self-Test (no acknowledgment required)
- 64-byte receive FIFO

**Footer:**
Espressif Systems  
ESP32-S3 Series Datasheet v2.1  
Page number: 54  
Submit Documentation Feedback