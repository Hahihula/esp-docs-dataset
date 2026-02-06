**Title: Peripherals**

- **Wrap TX mode**
- **Wrap RX mode**
- **Continuous TX mode**
- **DMA access for TX mode on channel 3**
- **DMA access for RX mode on channel 7**

For details, see [ESP32-S3 Technical Reference Manual](#) > Chapter Remote Control Peripheral.

---

**Title: Pin Assignment**

For RMT, the pins used can be chosen from any GPIOs via the GPIO Matrix. For more information about the pin assignment, see [ESP32-S3 Series Datasheet](#) > Section IO Pins and [ESP32-S3 Technical Reference Manual](#) > Chapter IO MUX and GPIO Matrix.

---

**Title: 5.2.1.13 Pulse Count Controller (PCNT)**

The pulse count controller (PCNT) captures pulse and counts pulse edges through multiple modes.

**Subtitle: Feature List**

- Four independent pulse counters (units) that count from 1 to 65535
- Each unit consists of two independent channels sharing one pulse counter
- All channels have input pulse signals (e.g., sig_ch0_un) with their corresponding control signals (e.g., ctrl_ch0_un)
- Independently filter glitches of input pulse signals (sig_ch0_un and sig_ch1_un) and control signals (ctrl_ch0_un and ctrl_ch1_un) on each unit
- Each channel has the following parameters:
  - Selection between counting on positive or negative edges of the input pulse signal
  - Configuration to Increment, Decrement, or Disable counter mode for control signal’s high and low states

For details, see [ESP32-S3 Technical Reference Manual](#) > Chapter Pulse Count Controller.

---

**Title: Pin Assignment**

For pulse count controller, the pins used can be chosen from any GPIOs via the GPIO Matrix. For more information about the pin assignment, see [ESP32-S3 Series Datasheet](#) > Section IO Pins and [ESP32-S3 Technical Reference Manual](#) > Chapter IO MUX and GPIO Matrix.

---

**Title: 5.2.2 Analog Signal Processing**

This subsection describes components on the chip that sense and process real-world data.
  
--- 

*Footer:* Espressif Systems, ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6

[Submit Documentation Feedback](#)