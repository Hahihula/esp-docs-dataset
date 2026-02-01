Title: Functional Description

Subtitle: PDM RX mode
- Raw PDM data reception
- PDM-to-PCM data format conversion (for I2S0 only), up to eight channels supported

Subtitle: Configurable APLL clock with frequencies up to 240 MHz

Subtitle: Configurable high-precision sample clock with a variety of sampling frequencies supported

Subtitle: 8/16/24/32-bit data width

Subtitle: Synchronous counter in TX mode

Subtitle: ETM feature

Subtitle: Direct Memory Access (GDMA-AHB only)

Subtitle: Standard I2S interface interrupts

Title: Pin Assignment
Body Text:
The pins for the I2S interfaces can be chosen from any GPIOs via the GPIO Matrix.

Subtitle: 4.2.2.7 LP I2S Controller
Body Text:
ESP32-P4 has a built-in LP I2S interface, which provides a data reception communication interface for Voice Activity Detection (VAD) and some digital audio applications in low power mode.

Title: Feature List

- RX master mode and slave mode
- A variety of audio standards supported:
  - TDM Philips standard
  - TDM MSB alignment standard
  - TDM PCM standard
  - PDM standard
- Various RX modes supported:
  - TDM RX mode, up to two channels supported
  - PDM RX mode

- Raw PDM data reception
- PDM-to-PCM data format conversion, up to two channels supported

Subtitle: Configurable sample clock with a variety of sampling frequencies supported

Subtitle: 16-bit data communication

Subtitle: Standard LP I2S interface interrupts

Footer:
Espressif Systems
Page Number and Document Information (partially obscured): ESP32-P4 Series Datasheet v0.6