**Title: Peripherals**

- **UART as the wake-up source**
- Software and hardware flow control

---

**Subtitle: Pin Assignment**

The pins connected to transmit and receive signals (UOTXD and UORXD) for UART0 are multiplexed with GPIO10 ~ GPIO11 via IO MUX. Other signals can be routed to any GPIOs via the GPIO matrix.

---

**Title: 5.2.1.2 SPI Controller**

ESP32-C61 has the following SPI interfaces:

- **SPI0**: used by ESP32-C61's cache and GDMA to access in-package or off-package flash/PSRAM
- **SPI1**: used by the CPU to access in-package or off-package flash/PSRAM

**SPI2**: is a general-purpose SPI controller with access to general-purpose DMA channels. SPI0 and SPI1 are reserved for system use, and only SPI2 is available for users.

---

**Subtitle: Features of SPI0 and SPI1**

- Supports Single SPI, Dual SPI, Quad SPI, QPI modes
- Data transmission is in bytes

---

**Subtitle: Features of SPI2**

- **As a master**
  - Supports operation as a master or slave
  - Support for DMA
  - Supports Single SPI, Dual SPI, Quad SPI, QPI modes
  - Configurable clock polarity (CPOL) and phase (CPHA)
  - Configurable clock frequency
  - Data transmission is in bytes
  - Configurable read and write data bit order: most-significant bit (MSB) first, or least-significant bit (LSB)

- **As a slave**
  - Supports Single SPI, Dual SPI, Quad SPI modes

---

**Footer**: Espressif Systems  
Submit Documentation Feedback ESP32-C61-MINI-I & MINI-1U Datasheet v0.6