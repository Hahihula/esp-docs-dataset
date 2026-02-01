**Title: Functional Description**

---

### **4.3.2 Wi-Fi**

The ESP32-S2 Wi-Fi radio and baseband support the following features:

- 802.11b/g/n

- 802.11n MCSO-7 that supports 20 MHz and 40 MHz bandwidth

- 802.11n MCS32

- 802.11n 0.4 µs guard-interval

- single stream, data rate up to 150 Mbps

- STBC RX (Single spatial stream)

- adjustable transmitting power

- antenna diversity
ESP32-S2 supports antenna diversity with an external RF switch. One or more GPIOs control the RF switch and select the best antenna to minimize the effects of channel imperfections.

### **4.3.2.1 Wi-Fi MAC**

ESP32-S2 implements the full 802.11 b/g/n Wi-Fi MAC protocol. It supports the Basic Service Set (BSS) STA and SoftAP operations under the Distributed Control Function (DCF). Power management is handled automatically with minimal host interaction to minimize the active-duty period.

The ESP32-S2 Wi-Fi MAC applies low-level protocol functions automatically. They are as follows:

- 4 × virtual Wi-Fi interfaces

- simultaneous Infrastructure BSS Station mode/SoftAP mode/Promiscuous mode

- RTS protection, CTS protection, Immediate Block ACK

- fragmentation and defragmentation

- TX/RX A-MPDU, RX A-MSDU

- TXOP

- WMM

- CCMP, TKIP, WAPI, WEP, BIP

- automatic beacon monitoring (hardware TSF)

- 802.11mc FTM

### **4.3.3 Networking Features**

Users are provided with libraries for TCP/IP networking, ESP-MESH networking, and other networking protocols over Wi-Fi. TLS 1.0, 1.1 and 1.2 support is also provided.

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

ESP32-S2 Series Datasheet v1.8