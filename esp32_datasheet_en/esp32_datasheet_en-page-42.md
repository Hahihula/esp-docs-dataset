**Title: Functional Description**

---

### Feature List

- Supports two external cards
- Supports SD Memory Card standard: version 3.0 and version 3.01)
- Supports SDIO Version 3.0
- Supports Consumer Electronics Advanced Transport Architecture (CE-ATA Version 1.1)
- Supports Multimedia Cards (MMC version 4.41, eMMC version 4.5 and version 4.51)

The controller allows up to 80 MHz clock output in three different data-bus modes: 1-bit, 4-bit, and 8-bit modes. It supports two SD/SDIO/MMC4.41 cards in a 4-bit data-bus mode. It also supports one SD card operating at 1.8 V.

For details, see [ESP32 Technical Reference Manual > Chapter SD/MMC Host Controller](#).

---

### Pin Assignment

The pins for SD/SDIO/MMC Host Controller are multiplexed with GPIO2, GPIO4, GPIO6 ~ GPIO15 via IO MUX.

For more information about the pin assignment, see Section 4.10 Peripheral Pin Configurations and [ESP32 Technical Reference Manual > Chapter IO_MUX and GPIO Matrix](#).

---

### SDIO/SPI Slave Controller (Section: 4.8.11)

ESP32 integrates an SD device interface that conforms to the industry-standard SDIO Card Specification Version 2.0, and allows a host controller to access the SoC, using the SDIO bus interface and protocol. ESP32 acts as the slave on the SDIO bus. The host can access the SDIO-interface registers directly and can access shared memory via a DMA engine, thus maximizing performance without engaging the processor cores.

#### Feature List

The SDIO/SPI slave controller supports the following features:

- SPI, 1-bit SDIO, and 4-bit SDIO transfer modes over the full clock range from 0 to 50 MHz
- Configurable sampling and driving clock edge
- Special registers for direct access by host
- Interrupts to host for initiating data transfer
- Automatic loading of SDIO bus data and automatic discarding of padding data
- Block size of up to 512 bytes
- Interrupt vectors between the host and the slave, allowing both to interrupt each other
- Supports DMA for data transfer

For details, see [ESP32 Technical Reference Manual > Chapter SDIO Slave Controller](#).

---

**Footer:**

Espressif Systems  
42 ESP32 Series Datasheet v5.2  

[Submit Documentation Feedback](#)