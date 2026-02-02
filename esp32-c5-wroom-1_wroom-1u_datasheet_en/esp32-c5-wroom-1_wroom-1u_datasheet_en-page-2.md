**Title:**
1 Module Overview

**Note (with QR code):**
Check the link or the QR code to make sure that you use the latest version of this document:
https://espressif.com/documentation/esp32-c5-wroom-1_wroom-1u_datasheet_en.pdf

---

**Subtitle 1: Features**

**Subsection Title:** CPU and On-Chip Memory
- ESP32-C5 embedded, 32-bit RISC-V single-core microprocessor, up to 240 MHz
- ROM: 320 KB
- HP SRAM: 384 KB
- LP SRAM: 16 KB

**Subsection Title:** Wi-Fi
- Operating frequency:
  - 1T1R in 2.4 and 5 GHz dual band (2412 ~ 2484 MHz, 5180 ~ 5885 MHz)
- IEEE 802.11ax-compliant

**Subsection Title:** Bluetooth®
- Fully compatible with IEEE 802.11b/g/n protocol:
  - 20 MHz and 40 MHz bandwidth
  - Data rate up to 150 Mbps
- Wi-Fi Multimedia (WMM)
- TX/RX A-MPDU, TX/RX A-MSDU

**Subsection Title:** Additional Features for Wi-Fi
- Immediate Block ACK
- Fragmentation and defragmentation
- Transmit opportunity (TXOP)

**Subsection Title:** Automatic Beacon monitoring (hardware TSF) - Four virtual Wi-Fi interfaces:
- Simultaneous support for Infrastructure BSS in Station mode, SoftAP mode, Station + SoftAP mode, and promiscuous mode

**Additional Information:**
- Note that when ESP32-C5 scans in Station mode, the SoftAP channel will change along with the Station channel
- Antenna diversity - 802.11mc FTM (Target wake time [TWT] that optimizes power saving mechanisms)

---

**Subtitle:** Wi-Fi

**Subsection Title:** IEEE 802.11ax-compliant:
- Operating frequency: 
  - Uplink and downlink OFDMA to enhance connectivity and performance in congested environments for IoT applications
- Downlink MU-MIMO (multi-user, multiple input, multiple output) to increase network capacity

**Subsection Title:** Bluetooth® Features:

**Subsection Title:** Additional Information:
- Beamformee that improves signal quality - Spatial reuse to maximize parallel transmissions.
- Target wake time [TWT] that optimizes power saving mechanisms.

**Subsection Title:** IEEE 802.11ac-compliant
- High power mode (20 dBm)
- Direction finding (AoA/AoD)

**Subsection Title:** Additional Information:
- Periodic advertising with responses (PAwR) - LE connection subrating

**Subsection Title:** Bluetooth® Features:

**Subsection Title:** Additional Information: 
- Downlink fullband MU-MIMO
- High power mode control.

---

**Footer:**
Espressif Systems  
ESP32-C5-WROOM-1 & WROOM-1U Datasheet v0.8  
Submit Documentation Feedback

PRELIMINARY