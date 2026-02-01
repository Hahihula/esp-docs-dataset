**Title: Functional Description**

The ESP32-C6 Wi-Fi MAC applies the following low-level protocol functions automatically:

- **4 × virtual Wi-Fi interfaces**
- Infrastructure BSS in Station mode, SoftAP mode, Station + SoftAP mode, and promiscuous mode

- RTS protection, CTS protection, Immediate Block ACK

- Fragmentation and defragmentation

- TX/RX A-MPDU, TX/RX A-MSDU

- Transmit opportunity (TXOP)

- Wi-Fi multimedia (WMM)

- GCMP, CCMP, TKIP, WAPI, WEP, BIP, WPA2-PSK/WPA2-Enterprise, and WPA3-PSK/WPA3-Enterprise

- Automatic beacon monitoring (hardware TSF)

- 802.11mc FTM

**Note:**
This feature is not supported in some chip revisions. See ESP32-C6 Series SoC Errata.

**Subtitle: 802.11ax supports:**

- Target wake time (TWT) requester
- Multiple BSSIDs
- Triggered response scheduling
- Uplink power headroom
- Operating mode
- Buffer status report

- Multi-user Request-to-Send (MU-RTS), Multi-user Block ACK Request (MU-BAR), and Multi-STA Block ACK (M-BA) frame

- Intra-PPDU power saving mechanism

- Two network allocation vectors (NAV)

- BSS coloring

- Spatial reuse

- Uplink power headroom

- Operating mode control

- Buffer status report

- TXOP duration RTS threshold

- UL-OFDMA random access (UORA)

**Footer:**
Espressif Systems
ESP32-C6 Series Datasheet v1.4