Title: Functional Description

Subtitle: 4.2.10 Remote Control Peripheral

Body Text:
The Remote Control Peripheral (RMT) supports two channels of infrared remote transmission and two channels of infrared remote reception. By controlling pulse waveform through software, it supports various infrared and other single wire protocols.

Subheading: Feature List
- four channels:
  - TX channels 0 ~ 1
  - RX channels 2 ~ 3
  - four channels share a 192 x 32-bit RAM

- the transmitter supports:
  - normal TX mode
  - wrap TX mode
  - modulation on TX pulses
  - continuous TX mode
  - multiple channels (programmable) transmitting data simultaneously

- the receiver supports:
  - normal RX mode
  - wrap RX mode
  - RX filtering
  - demodulation on RX pulses

For more details, see [ESP32-C5 Technical Reference Manual](#) > Chapter Remote Control Peripheral (RMT).

Subtitle: Pin Assignment

Body Text:
The pins for the Remote Control Peripheral can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see Section 2.3 IO Pins and [ESP32-C5 Technical Reference Manual](#) > Chapter GPIO Matrix and IO MUX.

Subtitle: 4.2.11 Parallel IO Controller

Body Text:
ESP32-C5 integrates a PARLIO controller for parallel data transfer. It has a transmitter and a receiver, connected with the GDMA controller. In full-duplex mode the PARLIO controller supports up to 4-bit parallel data transfer, while in half-duplex mode it supports up to 8-bit parallel data transfer.

Subheading: Feature List
- multiple clock sources and clock division, with clock frequency up to 40 MHz

Footer:
Espressif Systems | Page number (56) | Submit Documentation Feedback