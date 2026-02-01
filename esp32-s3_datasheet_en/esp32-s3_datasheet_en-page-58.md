**4 Functional Description**

---

### Pin Assignment

For details, see Section **2.3.5 Peripheral Pin Assignment**.

#### 4.2.1.11 Remote Control Peripheral (RMT)

The Remote Control Peripheral (RMT) is designed to send and receive infrared remote control signals.

##### Feature List
- Four TX channels
- Four RX channels
- Support multiple channels (programmable) transmitting data simultaneously
- Eight channels share a 384 x 32-bit RAM
- Support modulation on TX pulses
- Support filtering and demodulation on RX pulses
- Wrap TX mode
- Wrap RX mode
- Continuous TX mode
- DMA access for TX mode on channel 3
- DMA access for RX mode on channel 7

For details, see **ESP32-S3 Technical Reference Manual** > Chapter Remote Control Peripheral.

---

### Pin Assignment (Continued)

For details, see Section **2.3.5 Peripheral Pin Assignment**.

#### 4.2.1.12 Pulse Count Controller (PCNT)

The pulse count controller (PCNT) captures pulse and counts pulse edges through multiple modes.

##### Feature List
- Four independent pulse counters (units) that count from 1 to 65535
- Each unit consists of two independent channels sharing one pulse counter
- All channels have input pulse signals (e.g., sig_ch0_un) with their corresponding control signals (e.g. ctrl_ch0_un)
- Independently filter glitches of input pulse signals (sig_ch0_un and sig_ch1_un) and control signals (ctrl_ch0_un and ctrl_ch1_un) on each unit
- Each channel has the following parameters:
  - Selection between counting on positive or negative edges of the input pulse signal

Espressif Systems  
**58**  
[Submit Documentation Feedback](#)  
ESP32-S3 Series Datasheet v2.1