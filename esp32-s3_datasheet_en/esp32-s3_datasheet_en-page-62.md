**Title: Functional Description**

---

### **4.3.2.1 Wi-Fi Radio and Baseband**

The ESP32-S3 Wi-Fi radio and baseband support the following features:

- 802.11b/g/n

- 802.11n MCS0-7 that supports 20 MHz and 40 MHz bandwidth

- 802.11n MCS32

- 802.11n 0.4 µs guard-interval

- Data rate up to 150 Mbps

- RX STBC (single spatial stream)

- Adjustable transmitting power

**Antenna diversity:**  
ESP32-S3 supports antenna diversity with an external RF switch. This switch is controlled by one or more GPIOs, and used to select the best antenna to minimize the effects of channel imperfections.

---

### **4.3.2.2 Wi-Fi MAC**

ESP32-S3 implements the full 802.11b/g/n Wi-Fi MAC protocol. It supports the Basic Service Set (BSS) STA and SoftAP operations under the Distributed Control Function (DCF). Power management is handled automatically with minimal host interaction to minimize the active duty period.

The ESP32-S3 Wi-Fi MAC applies the following low-level protocol functions automatically:

- Four virtual Wi-Fi interfaces

- Simultaneous Infrastructure BSS Station mode, SoftAP mode, and Station + SoftAP mode

- RTS protection. CTS protection, Immediate Block ACK

- Fragmentation and defragmentation

- TX/RX A-MPDU, TX/RX A-MSDU

- TXOP

- WMM

  - GCMP, CCMP, TKIP, WAPI, WEP, BIP, WPA2-PSK/WPA2-Enterprise, and WPA3-PSK/WPA3-Enterprise

- Automatic beacon monitoring (hardware TSF)

- 802.11mc FTM

---

### **4.3.2.3 Networking Features**

Users are provided with libraries for TCP/IP networking, ESP-WIFI-MESH networking, and other networking protocols over Wi-Fi. TLS 1.2 support is also provided.

---

### **4.3.3 Bluetooth LE**

This subsection describes the chip's Bluetooth capabilities, which facilitate wireless communication for low-power, short-range applications. ESP32-S3 includes a Bluetooth Low Energy subsystem that integrates a

Espressif Systems

62
[Submit Documentation Feedback](#)