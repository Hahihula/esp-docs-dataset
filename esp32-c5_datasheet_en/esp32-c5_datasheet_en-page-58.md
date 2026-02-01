**Title: Functional Description**

- **Body Text:** 
  - data sources for output register bits: 64 bits of input data, two counters, LUT RAM data, data output of last cycle, comparators
  - with some restrictions, each of the 32 output register bits can come from any bit on the data sources

- **List Items:** 
  - 8 x 257-bit instruction memory, for storing eight instructions, controlling control flow and the data path
  - 2048 bytes of lookup table (LUT) memory, configurable as various word widths

**Reference Link:**
For more details, see [ESP32-C5 Technical Reference Manual](#) > Chapter BitScrambler.

---

**Title: Pin Assignment**

- **Body Text:** 
  The BitScrambler does not directly interact with IOs, so it has no pins assigned.
  
- For more information about the pin assignment, see Section [2.3 IO Pins](#) and [ESP32-C5 Technical Reference Manual](#) > Chapter GPIO Matrix and IO MUX.

---

**Title: 4.2.1.13 SDIO Slave Controller**

- **Body Text:** 
  The SDIO Slave controller in ESP32-C5 provides hardware support for the Secure Digital Input/Output (SDIO) device interface. It allows an SDIO host to access ESP32-C5 via an SDIO bus protocol.

---

**Title: Feature List**

- compatible with SDIO Physical Layer Specification V2.00 and SDIO Specifications V2.00
- support SPI, 1-bit SDIO, and 4-bit SDIO transfer modes
- clock range of 0 ~ 50 MHz
- configurable sample and drive clock edge
- integrated and SDIO-accessible registers for information interaction
- support SDIO interrupts
- automatic padding data and discarding the padded data on the SDIO bus
- block size up to 512 bytes
- interrupt vector between the host and slave for bidirectional interrupt
- support DMA for data transfer
- support wake-up from sleep when connection is retained

**Reference Link:**
For more details about the SDIO Slave controller, refer to the [ESP32-C5 Technical Reference Manual](#) > Chapter SDIO Slave Controller (SDIO).

---

**Title: Pin Assignment**

- **Body Text:** 
  The pins for the SDIO Slave controller are multiplexed with GPIO7 ~ GPIO10, GPIO13, and GPIO14 via IO MUX. GPIO13 ~ GPIO14 are also multiplexed with the pins for the USB serial/JTAG controller. The SDIO Slave controller can be used together with the USB Serial/JTAG controller in single SPI mode, but not in quad SPI mode.

---

**Footer:**
Espressif Systems  
[ESP32-C5 Series Datasheet v1.0](#)  
Submit Documentation Feedback