**Title: Peripherals**

For more details, see [ESP32-C5 Technical Reference Manual > Chapter Remote Control Peripheral (RMT)](#).

## Pin Assignment

The pins for the Remote Control Peripheral can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see:
- **[ESP32-C5 Series Datasheet > Section IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX](#)**

### 5.2.1.11 Parallel IO Controller

ESP32-C5 integrates a PARLIO controller for parallel data transfer. It has a transmitter and a receiver, connected with the GDMA controller.

- In full-duplex mode the PARLIO controller supports up to 4-bit parallel data transfer.
- While in half-duplex mode it supports up to 8-bit parallel data transfer.

#### Feature List
- multiple clock sources and clock division, with clock frequency up to 40 MHz
- receiver/transmitter supports input and output clock inverse

##### Additional Features:
- 1/2/4/8-bit data transfer
- changeable sample sequence for data to be transmitted and received in 1-bit, 2-bit, and 4-bit mode
- support for multiple data sampling mode by the receiver
- support for multiple GDMA EOF signal generation modes by the receiver

##### Output:
- output external chip select signals with configurable delay cycles
- support for transmitter clock gating

For more details about this assignment see [ESP32-C5 Technical Reference Manual > Chapter Parallel IO Controller](#).

## Pin Assignment (Repeated)

The pins for the Parallel IO controller can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see:
- **[ESP32-C5 Series Datasheet > Section IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX](#)**

### 5.2.1.12 BitScrambler

The ESP32-C5 has an extensive amount of DMA-capable peripherals.

These can move data from memory to external devices, or vice versa without any interference with the CPU.
This only works if:
- The device needs (or emits) the data in question is sent back as expected by software
- If not: The CPU must rewrite format for example swap bytes, reverse bytes and shift left/right.

As bit-wise operations tend to be fairly CPU-expensive,
the purpose of DMA includes using it when transferring between memory or peripheral.
The RX channel dedicated only transfers from memory-to-peripheral; the TX is used exclusively in memory-to-peripheral transfer. The BitScrambler can perform these tasks efficiently, as described above.

Espressif Systems

ESP32-C5-MINI-1 Datasheet v1.0
Submit Documentation Feedback