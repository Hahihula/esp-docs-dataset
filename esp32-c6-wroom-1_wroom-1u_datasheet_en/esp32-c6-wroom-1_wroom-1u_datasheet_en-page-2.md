**Title:**
1 Module Overview

**Note (with link to document):**
Check the link or the QR code to make sure that you use the latest version of this document:
https://espressif.com/documentation/esp32-c6-wroom-1_wroom-1u_datasheet_en.pdf

**Subtitle 1.1: Features**

**Subheading CPU and On-Chip Memory**
- ESP32-C6 embedded, 32-bit RISC-V single-core microprocessor, up to 160 MHz
- ROM: 320 KB
- HP SRAM: 512 KB
- LP SRAM: 16 KB

**Subheading Wi-Fi**
- 1T1R in 2.4 GHz band
- Operating frequency: 2412 ~ 2484 MHz
- IEEE 802.11ax-compliant:
  - 20 MHz-only non-AP mode
  - MCS0 ~ MCS9

**Subheading Wi-Fi (continued)**
- Uplink and downlink OFDMA, especially suitable for simultaneous connections in high-density environments
- Downlink MU-MIMO (multi-user, multiple input, multiple output) to increase network capacity:
  - Beamformee that improves signal quality
  - Channel quality indication (CQI)
  - DCM (dual carrier modulation) to improve link robustness

**Subheading Wi-Fi (continued)**
- Spatial reuse to maximize parallel transmissions
- Target wake time (TWT) that optimizes power saving mechanisms:
  - Fully compatible with IEEE 802.11b/g/n protocol

**Subheading Bluetooth®**
- Data rate up to 150 Mbps
- Wi-Fi Multimedia (WMM)
- TX/RX A-MPDU, TX/RX A-MSDU
- Immediate Block ACK
- Fragmentation and defragmentation
- Transmit opportunity (TXOP)
- Automatic Beacon monitoring (hardware TSF)
- 4 × virtual Wi-Fi interfaces

**Subheading Bluetooth®**
- Simultaneous support for Infrastructure BSS in Station mode, SoftAP mode, Station + SoftAP mode, and promiscuous mode:
  - Note that when ESP32-C6 scans in Station mode, the SoftAP channel will change along with the Station channel
- 802.11mc FTM

**Subheading Bluetooth®**
- Bluetooth LE: Bluetooth 5.3 certified
- Bluetooth mesh
- High power mode (20 dBm)
- Speed: 125 Kbps, 500 Kbps, 1 Mbps, 2 Mbps
- Advertising extensions
- Multiple advertisement sets
- Channel selection algorithm #2
- LE power control

**Footer Information**
Espressif Systems  
Page number and document version:
ESP32-C6-WROOM-1 & WROOM-1U Datasheet v1.4  

**Link to Submit Documentation Feedback:**
[Submit Documentation Feedback](#)