**Title: RF Characteristics**

---

### Table 7-11 – cont’d from previous page

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| Carrier frequency drift | \( \left\lvert f_0 - f_n \right\rvert_{n=1,2,...k} \) | — | 1.37 | — | kHz |
| | \( \left\lvert f_0 - f_3 \right\rvert \) | — | 1.09 | — | kHz |
| | \( \left\lvert f_n - f_{n-3} \right\rvert_{n=7,8,...k} \) | — | 0.51 | — | kHz |

---

### Subtitle: 7.2.2 Bluetooth LE RF Receiver (RX) Characteristics

---

#### Table 7-12. Bluetooth LE - Receiver Characteristic - 1 Mbps

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| Sensitivity @30.8% PER | — | — | –96 | — | dBm |
| Maximum received signal @30.8% PER | — | 5 | — | — | dBm |
| Co-channel C/I | F = FO + 1 MHz | −4 | — | — | dB |
| | F = FO − 1 MHz | −3 | — | — | dB |
| Adjacent channel selectivity C/I | F = FO + 2 MHz | −32 | — | — | dB |
| | F = FO − 2 MHz | −36 | — | — | dB |
| | F ≥ FO + 3 MHz(1) | — | — | — | dB |
| | F ≤ FO − 3 MHz | −39 | — | — | dB |
| Image frequency | \( F = F_{image} \pm 1 MHz \) | −29 | — | — | dB |
| Adjacent channel to image frequency | \( F = F_{image} - 1 MHz \) | −34 | — | — | dB |
| | 30 MHz ~ 2000 MHz | −9 | — | — | dBm |
| Out-of-band blocking performance | 2003 MHz ~ 2399 MHz | −18 | — | — | dBm |
| | 2484 MHz ~ 2997 MHz | −16 | — | — | dBm |
| Intermodulation | 3000 MHz ~ 12.75 GHz | −6 | — | — | dBm |

**Footnote:**
1 Refer to the value of Adjacent channel to image frequency when F = \( F_{image} \) ≈ 1 MHz.

---

#### Table 7-13. Bluetooth LE - Receiver Characteristic - 2 Mbps

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| Sensitivity @30.8% PER | — | — | –93 | — | dBm |
| Maximum received signal @30.8% PER | 2 | − | 2 | — | dBm |
| Co-channel C/I | F = FO + 2 MHz | −7 | — | — | dB |
| | F = FO − 2 MHz | −7 | — | — | dB |
| Adjacent channel selectivity C/I | F = FO + 4 MHz(1) | — | — | — | dB |
| | F = FO − 4 MHz | −34 | — | — | dB |
| Image frequency | \( F = F_{image} \pm 2 MHz \) | −27 | — | — | dB |
| Adjacent channel to image frequency | (Continued on next page) | -39 | — | — | dB |

---

**Footer:**
Espressif Systems
ESP8685-WROOM-01 Datasheet v1.5

Submit Documentation Feedback