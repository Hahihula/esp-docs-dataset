**1 Module Overview**

### Features

#### CPU and On-Chip Memory
- ESP32-C61 embedded, 32-bit RISC-V single-core microprocessor, up to 160 MHz
- ROM: 256 KB
- SRAM: 320 KB

#### Wi-Fi
- 802.11r in 2.4 GHz band
- Operating frequency: 2412 ~ 2484 MHz
- IEEE 802.11ax-compliant:
  - 20 MHz-only non-AP mode
  - MCS0 ~ MCS9

##### Details about Wi-Fi (continued)
- Uplink and downlink OFDMA, especially suitable for simultaneous connections in high-density environments.
- Downlink MU-MIMO (multi-user, multiple input, multiple output) to increase network capacity.

##### Additional Features of Wi-Fi:
- Beamformer that improves signal quality
- Channel quality indication (CQI)
- DCM (dual carrier modulation) to improve link robustness
- Spatial reuse to maximize parallel transmissions.
- Target wake time (TWT) that optimizes power saving mechanisms

#### Fully compatible with IEEE 802.11b/g/n protocol:
- 20 MHz and 40 MHz bandwidth
- Data rate up to 150 Mbps
- Wi-Fi Multimedia (WMM)
- TX/RX A-MPDU, TX/RX A-MSDU

#### Bluetooth®
- Bluetooth LE: Bluetooth 5.3 certified.
- Bluetooth mesh.

##### Additional Features of Bluetooth:
- High power mode (20 dBm).
- Speeds available are 125 Kbps, 500 Kbps, 1 Mbps, and 2 Mbps.
- Advertising extensions.
- Multiple advertisement sets
- Channel selection algorithm #2

#### Power Control Mechanism between Wi-Fi and Bluetooth:
- Internal co-existence mechanism that allows them to share the same antenna.

##### Peripherals included in ESP32-C61:
- GPIO, SPI, UART, I2C, I2S, LED PWM, USB Serial/JTAG controller, GDMA.
- On-chip debug functionality via JTAG; event task matrix, ADC temperature sensor,
- Brown-out detector
- Analog voltage comparator;
- General-purpose timers system timer and watchdog timers

**Espressif Systems**
Submit Documentation Feedback ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6