**Title: Functional Description**

For more information about the pin assignment, see Section **2.3 IO Pins**.

---

### Subtitle: SDIO Slave Controller

#### Section Number and Title:
4.2.17 SDIO Slave Controller

The SDIO Slave controller in ESP32-C61 provides hardware support for the Secure Digital Input/Output (SDIO) device interface. It allows an SDIO host to access ESP32-C61 via an SDIO bus protocol.

#### Feature List:
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

#### Subsection: Pin Assignment

The pins for the SDIO Slave controller are multiplexed with GPIO22 ~ GPIO23, and GPIO25 ~ GPIO28 via IO MUX.

For more information about the pin assignment, see Section **2.3 IO Pins**.

---

### Subtitle: Analog Signal Processing

#### Section Number:
4.2.2 An analog signal processing

This subsection describes components on the chip that sense and process real-world data.

#### Subsection Title with Page Reference:
4.2.2.1 SAR ADC
ESP32-C61 integrates a Successive Approximation Analog-to-Digital Converter (SAR ADC) to convert analog signals into digital representations.

#### Feature List:

- 12-bit sampling resolution
- Analog voltage sampling from up to four pins
- Attenuation of input signals for voltage conversion
- Software-triggered one-time sampling
- Timer-triggered multi-channel scanning

---

**Footer:**
Espressif Systems  
Page Number and Document Version:
48 ESP32-C61 Series Datasheet v0.5