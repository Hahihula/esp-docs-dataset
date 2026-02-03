**Title: Functional Description**

---

### **4.6.5 Wi-Fi MAC**

The ESP32 Wi-Fi MAC applies low-level protocol functions automatically. They are as follows:

- Four virtual Wi-Fi interfaces
- Simultaneous Infrastructure BSS Station mode/SoftAP mode/Promiscuous mode
- RTS protection, CTS protection, Immediate Block ACK

#### Subsections:
- Defragmentation
- TX/RX A-MPDU, RX A-MSDU
- TXOP
- WMM
- CCMP (CBC-MAC, counter mode), TKIP (MIC, RC4), WAPI (SMS4), WEP (RC4) and CRC

#### Additional Features:
- Automatic beacon monitoring (hardware TSF)

---

### **4.7 Bluetooth**

The chip integrates a Bluetooth Link controller and Bluetooth baseband, which carry out the baseband protocols and other low-level link routines, such as modulation/demodulation, packet processing, bit stream processing, frequency hopping, etc.

#### Subsection: 4.71 Bluetooth Radio and Baseband

The Bluetooth Radio and Baseband support the following features:

- Class-1, class-2 and class-3 transmit output powers, and a dynamic control range of up to 21 dB
- π/4 DQPSK and 8 DPSK modulation
- High performance in NZIF receiver sensitivity with a minimum sensitivity of -94 dBm

#### Additional Features:
- Class-1 operation without external PA
- Internal SRAM allows full-speed data-transfer, mixed voice and data, and full piconet operation
- Logic for forward error correction, header error control, access code correlation, CRC, demodulation, encryption bit stream generation, whitening and transmit pulse shaping

##### Features List:
- ACL, SCO, eSCO, and AFH
- A-law, μ-law, and CVSD digital audio CODEC in PCM interface
- SBC audio CODEC
- Power management for low-power applications
- SMP with 128-bit AES

---

### **4.7.2 Bluetooth Interface**

Provides UART HCI interface, up to 4 Mbps.

Provides SDIO/SPI HCI interface

---

**Footer:**
Espressif Systems  
34  
ESP32 Series Datasheet v5.2  

[Submit Documentation Feedback](#)