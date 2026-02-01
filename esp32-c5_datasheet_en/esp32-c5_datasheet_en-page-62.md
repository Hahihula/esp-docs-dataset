**Title: Functional Description**

---

### **4.3.2.1 Wi-Fi Radio and Baseband**

The ESP32-C5 Wi-Fi radio and baseband support the following features:

- compliant with IEEE 802.11a/b/g/n/ac/ax

#### *1T1R in 2.4 GHz and 5 GHz dual band*

- **802.11ax**
  - 20 MHz-only non-AP mode
    - MCS0 ~ MCS9 in 2.4 GHz band
    - MCS0 ~ MCS7 in 5 GHz band
  - uplink and downlink OFDMA

#### *downlink MU-MIMO (multi-user, multiple input, multiple output)*

- longer OFDM symbol, with 0.8, 1.6, and 3.2 µs guard interval

#### *DCM (dual carrier modulation), up to 16-QAM*

- single-user/multi-user beamformee
- channel quality indication (CQI)
- RX STBC (single spatial stream)

#### **802.11ac**
  - MCS0 ~ MCS7 that support 20 MHz bandwidth

#### *downlink fullband MU-MIMO (multi-user, multiple input, multiple output)*

- single-user/multi-user beamformee
- RX STBC (single spatial stream)
- 0.4 µs guard interval

#### **802.11a/b/g/n**

- MCS0 ~ MCS7 that support 20 MHz and 40 MHz bandwidth
- MCS32
- data rate up to 150 Mbps
- 0.4 µs guard interval

- adjustable transmitting power

- antenna diversity: ESP32-C5 supports antenna diversity with an external RF switch. This switch is controlled by one or more GPIOs, and used to select the best antenna to minimize the effects of channel imperfections.

---

**Footer:**  
Espressif Systems  
62  
ESP32-C5 Series Datasheet v1.0  

[Submit Documentation Feedback](#)