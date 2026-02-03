**Title: Electrical Characteristics**

---

### Parameter Table

| **Parameter** | Description | Min | Typ | Max | Unit |
|---------------|-------------|-----|-----|-----|------|
| 11n, HT20, MCSO | — | —93 | dBm |
| 11n, HT20, MCS7 | —73 | dBm |
| 11n, HT40, MCSO | —90 | dBm |
| 11n, HT40, MCS7 | —70 | dBm |
| Adjacent channel rejection | 11g, 6 Mbps | 27 | dB |
| Adjacent channel rejection | 11g, 54 Mbps | 13 | dB |

---

**Body Text:**

1. Device should operate in the frequency range allocated by regional regulatory authorities. Target operating frequency range is configurable by software.
2. The typical value of the Wi-Fi radio output impedance is different between chips in different QFN packages. For chips in a QFN 6x6 package, the value is 30+j10 Ω. For chips in a QFN 5x5 package, the value is 35+j10 Ω.
3. Target TX power is configurable based on device or certification requirements.

---

**Subtitle: Bluetooth Radio**

### Subsection Title: Receiver – Basic Data Rate

#### Table (Table 5-7): Receiver Characteristics - Basic Data Rate

| **Parameter** | Description | Min | Typ | Max | Unit |
|----------------|-------------|-----|-----|-----|------|
| Sensitivity @0.1% BER | — | —90 | dBm |
| Maximum received signal @0.1% BER | 0 | — | dBm |
| Co-channel C/I | F = FO + 1 MHz | — | —6 | dB |
| Adjacent channel selectivity C/I | F = FO –1 MHz | — | —6 | dB |
| Adjacent channel selectivity C/I | F = FO + 2 MHz | — | —25 | dB |
| Adjacent channel selectivity C/I | F = FO –2 MHz | — | —33 | dB |
| Adjacent channel selectivity C/I | F = FO + 3 MHz | — | —25 | dB |
| Adjacent channel selectivity C/I | F = FO –3 MHz | — | —45 | dB |
| Out-of-band blocking performance (30 MHz ~ 2000 MHz) | -10 | dBm |
| Out-of-band blocking performance (2000 MHz ~ 2400 MHz) | -27 | dBm |
| Out-of-band blocking performance (2500 MHz ~ 3000 MHz) | -27 | dBm |
| Intermodulation | —10 | dBm |

---

**Subtitle: Transmitter – Basic Data Rate**

#### Table (Table 5-8): Transmitter Characteristics - Basic Data Rate

| **Parameter** | Description | Min | Typ | Max | Unit |
|----------------|-------------|-----|-----|-----|------|
| RF transmit power note1 | — | 0 | dBm |
| Gain control step | — | 3 | dB |

---

*Note: The text "note1" is likely a reference to additional information or conditions related to the parameter.*

**Footer Information:**  
Espressif Systems  
ESP32 Series Datasheet v5.2  
Submit Documentation Feedback

Page Number: **55**