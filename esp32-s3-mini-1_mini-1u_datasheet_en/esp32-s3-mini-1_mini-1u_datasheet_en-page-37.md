**Title: RF Characteristics**

---

### Table 7-11. Bluetooth LE - Transmitter Characteristics - 600 Kbps

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| Carrier frequency offset and drift | \( \max |f_n|_{n=0, 1, 2,...k} \) | — | 0.80 | — | kHz |
| | Maximum | \( f_0 - f_n \) | 1.00 | — | kHz |
| Modulation characteristics | \( |f_n - f_{n-3}| \) | — | 0.85 | — | kHz |
| In-band spurious emissions | \( |f_0 - f_3| \) | Minimum \( \Delta f_{2\text{avg}} \) (for at least 99.9% of all \( \Delta f_{2\text{max}} \)) | Maximum: 213.00 kHz, Min: — | — | kHz |
| & | Minimum \( \Delta f_2\text{max} \) for at least 99.9% of all \( \Delta f_2\text{max} \) | Max: 196.00 kHz, Min: — | — | kHz |
| & | ±3 MHz offset | -37.00 dBm to +45.00 dBm (typical range for Bluetooth LE) | Minimum: −42.00 dBm; Maximum: −44.00 dBm | dBm |

---

**Subtitle 7.2.2**: **Bluetooth LE RF Receiver (RX) Characteristics**

### Table 7-12. Bluetooth LE - Receiver Characteristics - 1 Mbps

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| Sensitivity @30.8% PER | — | Minimum: −96.5 dBm, Maximum: — | — | — | dBm |
| Maximum received signal @30.8% PER | 8 | F = FO MHz | 8 | — | dBm |
| Co-channel C/I | \( \text{F} = \text{FO} + 1\ \text{MHz} \) | Minimum: −4 dB, Maximum: ∞ | -4 dB to ∞ | dB |
| & | \( \text{F} = \text{FO} - 1\ \text{MHz} \) | — | –23 dB to ∞ | dB |
| Adjacent channel selectivity C/I | \( \text{F} = \text{FO} + 2\ \text{MHz} \) | Minimum: −4 dB, Maximum: ∞ | -4 dB to ∞ | dB |
| & | \( \text{F} = \text{FO} - 2\ \text{MHz} \) | — | –23 dB to ∞ | dB |
| Adjacent channel selectivity C/I (continued) | \( \text{F} = \text{FO} + 3\ \text{MHz} \) | Minimum: −4 dB, Maximum: ∞ | -4 dB to ∞ | dB |
| & | \( \text{F} = \text{FO} - 3\ \text{MHz} \) | — | –29 dB to ∞ | dB |
| Image frequency (continued) | F > FO + 3 MHz, Minimum: −4 dB, Maximum: ∞ | Min: −36 dB, Max: ∞ | -37 dB to ∞ | dB |
| & | \( \text{F} = \text{FO} - 3\ \text{MHz} \) | — | –29 dB to ∞ | dB |

---

**Subtitle**: **Intermodulation**

### Table 7-13. Bluetooth LE - Receiver Characteristics - 2 Mbps

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| Sensitivity @30.8% PER | — | Minimum: −92 dBm, Maximum: ∞ | — | — | dBm |
| Maximum received signal @30.8% PER (continued) | 3 | F = FO MHz to +45.00 dBm typical range for Bluetooth LE; Min: -16 dBm and Max: −92 dBm, Minimum: ∞ | –3 dBM to ∞ | — | dBm |

---

**Footer**: Espressif Systems  
Page 37  
ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6

Submit Documentation Feedback