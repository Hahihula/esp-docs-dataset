**Title: Functional Description**

- receiver/transmitter supports input and output clock inverse

- **1/2/4/8-bit data transfer**
  
- changeable sample sequence for data to be transmitted and received in 1-bit, 2-bit, and 4-bit mode
  
- support for multiple data sampling mode by the receiver
  
- support for multiple GDMA EOF signal generation modes by the receiver
  
- output external chip select signals with configurable delay cycles
  
- support for transmitter clock gating

**For more details, see ESP32-C5 Technical Reference Manual > Chapter Parallel IO Controller.**

---

**Subtitle: Pin Assignment**

The pins for the Parallel IO controller can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see Section 2.3 IO Pins and [ESP32-C5 Technical Reference Manual](#) > Chapter GPIO Matrix and IO MUX.

---

**Title: 4.2.1.12 BitScrambler**

The ESP32-C5 has an extensive amount of DMA-capable peripherals. These can move data from memory to an external device, and vice versa, without any interference from the CPU. This only works if the external device needs or emits the data in question in the same format as the software expects it: if not, the CPU needs to rewrite the format of the data.

Examples include a need to swap bytes, reverse bytes, and shift the data left or right.

As bitwise operations tend to be fairly CPU-expensive and the purpose of DMA is to not use the CPU in the transfer, ESP32-C5 integrates one BitScrambler, which are dedicated peripherals that change the format of data between memory and the peripheral. The RX channel is dedicated to peripheral-to-memory transfers, and the TX channel is dedicated to memory-to-peripheral transfers.

The BitScrambler is capable of performing the aforementioned operations but as a flexible programmable state machine it can be used for more advanced things too

---

**Subtitle: Feature List**

- one BitScrambler, one channel for RX (peripheral-to-memory), one channel for TX (memory-to-peripheral). The two channels support only half-duplex communications and cannot work at the same time
  
- **support for memory-to-memory transfers**
  
- process up to 32 bits per DMA clock period
  
- data path controlled by a BitScrambler program stored in the instruction memory
  
- input registers able to read 0, 8, 16, or 32 bits per clock cycle
  
- output registers:
  - **able to write 0, 8, 16, or 32 bits per clock cycle**

---

**Footer:**
Espressif Systems
ESP32-C5 Series Datasheet v1.0

[Submit Documentation Feedback](#)