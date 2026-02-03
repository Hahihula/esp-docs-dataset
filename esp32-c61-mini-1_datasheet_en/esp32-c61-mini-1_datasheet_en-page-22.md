**Title: Peripherals**

---

### Feature List

- Generating digital waveform with configurable periods and duty cycle. The resolution of duty cycle can be up to 20 bits.
- Multiple clock sources, including 80 MHz PLL clock, external main crystal clock, and internal fast RC oscillator.
- Operation when the CPU is in Light-sleep mode
- Gradual increase or decrease of duty cycle, which is useful for the LED RGB color-gradient generator
- Up to 16 duty cycle ranges for gamma curve generation; each can be independently configured in terms of duty cycle direction (increase or decrease), step size, the number of steps, and step frequency

---

### Pin Assignment

The pins for the LED PWM Controller can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see [ESP32-C61 Series Datasheet > Section 10 Pins](#).

---

**Subtitle: 5.2.1.7 SDIO Slave Controller**

The SDIO Slave controller in ESP32-C61 provides hardware support for the Secure Digital Input/Output (SDIO) device interface. It allows an SDIO host to access ESP32-C61 via an SDIO bus protocol.

---

### Feature List

- compatible with SDIO Physical Layer Specification V2.00 and SDIO Specifications V2.00
- support SPI, 1-bit SDIO, and 4-bit SDIO transfer modes
- clock range of 0 ~ 50 MHz.
- configurable sample and drive clock edge
- integrated and SDIO-accessible registers for information interaction
- support SDIO interrupts
- automatic padding data and discarding the padded data on the SDIO bus
- block size up to 512 bytes
- interrupt vector between the host and slave for bidirectional interrupt
- support DMA for data transfer
- support wake-up from sleep when connection is retained

---

### Pin Assignment

The pins for the SDIO Slave controller are multiplexed with GPIO22 ~ GPIO23, and GPIO25 ~ GPIO28 via IO MUX.

For more information about the pin assignment, see [ESP32-C61 Series Datasheet > Section 10 Pins](#).

---

**Footer:**

Espressif Systems  
Page number: 22  
Document version: ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6

[Submit Documentation Feedback](#)