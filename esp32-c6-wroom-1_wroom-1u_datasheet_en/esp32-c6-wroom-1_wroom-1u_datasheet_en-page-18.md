**Title: Peripherals**

- High-speed data communication using GDMA (not supported by LP UART)
- Receive timeout feature
- UART as the wake-up source
- Software and hardware flow control

---

**Subtitle: Pin Assignment**

For details, see [ESP32-C6 Series Datasheet](#) > Section Peripheral Pin Assignment.

---

**Title: 5.2.1.2 SPI Controller**

ESP32-C6 has the following SPI interfaces:

- **SPI0**: used by ESP32-C6's cache and GDMA to access in-package or off-package flash
- **SPI1**: used by the CPU to access in-package or off-package flash

**Note:** SPI2 is a general-purpose SPI controller with access to general-purpose DMA channels. SPI0 and SPI1 are reserved for system use, and only SPI2 is available for users.

---

**Subtitle: Features of SPI0 and SPI1**

- Supports Single SPI, Dual SPI, Quad SPI (QPI) modes
- Data transmission is in bytes

---

**Subtitle: Features of SPI2**

- Supports operation as a master or slave
- Support for GDMA
- Supports Single SPI, Dual SPI, Quad SPI (QPI) modes
- Configurable clock polarity (CPOL) and phase (CPHA)
- Configurable clock frequency
- Data transmission is in bytes
- Configurable read and write data bit order: most-significant bit (MSB) first, or least-significant bit (LSB) first

**As a master**
  - Supports 2-line full-duplex communication with clock frequency up to 80 MHz
  - Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 80 MHz
  - Provides six FSPICS... pins for connection with six independent SPI slaves

**As a slave**
  - Configurable CS setup time and hold time

---

**Supports full-duplex communication with clock frequency up to 40 MHz**

---

Espressif Systems  
18 ESP32-C6-WROOM-1 & WROOM-1U Datasheet v1.4  

[Submit Documentation Feedback](#)