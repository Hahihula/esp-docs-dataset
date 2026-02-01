**Title: Functional Description**

---

### Subtitle: Wi-Fi MAC

ESP32-C5 implements the full IEEE 802.11a/b/g/n/ac/ax Wi-Fi MAC protocol. It supports the Basic Service Set (BSS) STA and SoftAP operations under the Enhanced Distributed Channel Access (EDCA). Power management is handled automatically with minimal host interaction to minimize the active duty period.

The ESP32-C5 Wi-Fi MAC applies the following low-level protocol functions automatically:

- four virtual Wi-Fi interfaces
- infrastructure BSS in Station mode, SoftAP mode, Station + SoftAP mode, and promiscuous mode
- RTS protection, CTS-to-Self protection, immediate block ACK
- fragmentation and defragmentation
- TX/RX A-MPDU, TX/RX A-MSDU
- transmission opportunity (TXOP)
- Wi-Fi multimedia (WMM)
- GCMP, CCMP, TKIP, WAPI, WEP, BIP, WPA2-PSK, and WPA3-PSK
- automatic beacon monitoring (hardware TSF)
- 802.11mc FTM

**Subtitle: 802.11ax supports**

- target wake time (TWT) requester
- multiple BSSIDs
- triggered response scheduling
- Multi-User Request-to-Send (MU-RTS), Multi-User Block ACK Request (MU-BAR), and Multi-STA Block ACK (M-BA) frame
- intra-PPDU power saving mechanism
- two network allocation vectors (NAV)
- BSS coloring
- spatial reuse
- uplink power headroom
- operating mode control
- buffer status report
- TXOP duration RTS threshold
- UL-OFDMA random access (UORA)

---

### Subtitle: Networking Features

Espressif provides libraries for TCP/IP networking, ESP-WIFI-MESH networking, and other networking protocols over Wi-Fi. TLS 1.0, 1.1, and 1.2 are also supported.

---

**Footer:**  
Espressif Systems  
63  
ESP32-C5 Series Datasheet v1.0

[Submit Documentation Feedback](#)