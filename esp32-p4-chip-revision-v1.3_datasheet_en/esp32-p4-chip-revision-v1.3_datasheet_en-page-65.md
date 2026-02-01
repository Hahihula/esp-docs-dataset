**Title: Functional Description**

---

### Section Title

#### Subsection (4.2.2.5) I3C Controller

ESP32-P4 includes one I3C master interface.

- **Feature List**
  - The I3C master interface supports the following features:
    - Compliant with I3C protocol
    - Compatible with I2C mode (FM, FM+)
    - SDR mode
    - Dynamic address allocation
    - In-Band interrupts
    - DMA transfer

- **Pin Assignment**
  For I3C master interface, the pins for clock and data signals are multiplexed with GPIO32–GPIO33 via the GPIO matrix. Other signals can be routed to any GPIOs via the GPIO matrix.

---

#### Subsection (4.2.2.6) I2S Controller (I2S)

ESP32-P4 has three built-in I2S interfaces, which provide flexible communication interfaces for streaming digital data in multimedia applications, especially digital audio applications.

- **Feature List**
  - Master mode and slave mode
  - Full-duplex and half-duplex communications
  - Separate TX and RX units that can work independently or simultaneously.
  - A variety of audio standards supported:
    - TDM Philips standard
    - TDM MSB alignment standard
    - TDM PCM standard
    - PDM standard

- **Various TX/RX modes supported:**
  - TDM TX mode, up to 16 channels supported
  - TDM RX mode, up to 16 channels supported
  - PDM TX mode
    - Raw PDM data transmission
    - PCM-to-PDM data format conversion (for I2S0 only), up to two channels supported

---

**Footer:**
- Page number and document information:
  - "Espressif Systems"
  - Document version note at the bottom right corner.
  - Link for submitting documentation feedback.