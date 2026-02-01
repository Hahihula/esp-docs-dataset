**Title: Functional Description**

---

### **4.3.2.1 Wi-Fi Radio and Baseband**

The ESP32-C61 Wi-Fi radio and baseband support the following features:

- 1T1R in 2.4 GHz band

#### *802.11ax*

- 20 MHz-only non-AP mode
- MCS0 ~ MCS9
- Uplink and downlink OFDMA
- Downlink MU-MIMO (multi-user, multiple input, multiple output)
- Longer OFDM symbol, with 0.8, 1.6, 3.2 µs guard interval
- DCM (dual carrier modulation), up to 16-QAM
- Single-user/multi-user beamformee
- Channel quality indication (CQI)
- RX STBC (single spatial stream)

#### *802.11b/g/n*

- MCS0 ~ MCS7 that supports 20 MHz and 40 MHz bandwidth
- MCS32
- Data rate up to 150 Mbps
- 0.4 µs guard interval

- Adjustable transmitting power
- Antenna diversity: ESP32-C61 supports antenna diversity with an external RF switch. This switch is controlled by one or more GPIOs, and used to select the best antenna to minimize the effects of channel imperfections.

---

### **4.3.2.2 Wi-Fi MAC**

ESP32-C61 implements the full IEEE 802.11 b/g/n/ax Wi-Fi MAC protocol. ESP32-C61 supports the Basic Service Set (BSS) STA and SoftAP operations under the Enhanced Distributed Channel Access (EDCA). Power management is handled automatically with minimal host interaction to minimize the active duty period.

The ESP32-C61 Wi-Fi MAC applies the following low-level protocol functions automatically:

- Four virtual Wi-Fi interfaces
- Infrastructure BSS in Station mode, SoftAP mode, Station + SoftAP mode, and promiscuous mode
- RTS protection, CTS-to-Self protection, Immediate Block ACK

- Fragmentation and defragmentation
- TX/RX A-MPDU, TX/RX A-MSDU
- Transmit opportunity (TXOP)

---

**Footer:**
Espressif Systems  
52 ESP32-C61 Series Datasheet v0.5