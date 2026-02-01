**Title: Functional Description**

- RX filtering
- Demodulation on RX pulses
- GDMA access supported by RX channel 7

---

**Subtitle: Pin Assignment**

The pins for the remote control peripheral can be chosen from any GPIOs via the GPIO Matrix.

---

**Section Title: 4.2.2.18 Parallel IO Controller (PARLIO)**

ESP32-P4 contains a Parallel IO controller (PARLIO) capable of transferring data between external devices and internal memory on a parallel bus through General Direct Memory Access (GDMA).

**Subtitle: Feature List**

- Various clock sources:
  - Including external IO clock PAD_CLK_TX/RX and internal system clock XTAL_CLK, PLL_F160M_CLK, and RC_FAST_CLK
  - Maximum IO clock frequency of 40 MHz
  - Integer and fractional clock frequency division

- 1/2/4/8/16-bit configurable data bus width

- Full-duplex communication with 16-bit data bus width

- Bit reversal when data bus width is 1/2/4-bit

- RX unit for receiving IO parallel data, which supports:
  - Output clock gating
  - RX unit input and output clock inverse
  - Various receive modes
  - Configurable GDMA SUC EOF generation

- TX unit for sending IO parallel data, which supports:
  - Output clock gating
  - TX unit input and output clock inverse
  - Configurable TX EOF generation
  - Valid signal output
  - Configurable bus idle value

**Subtitle: Pin Assignment**

The pins for the parallel IO controller can be chosen from any GPIOs via the GPIO Matrix.

---

**Footer Information**
- Page number: 75
- Document title: ESP32-P4 Series Datasheet v0.6
- Company name: Espressif Systems

[Submit Documentation Feedback](#)