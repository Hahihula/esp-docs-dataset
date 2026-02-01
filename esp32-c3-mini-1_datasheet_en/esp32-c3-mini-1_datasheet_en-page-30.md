**Title: RF Characteristics**

---

### Table 7-11. Bluetooth LE - Transmitter Characteristics - 500 Kbps

| Parameter                | Description                   | Min   | Typ    | Max     | Unit |
|--------------------------|-------------------------------|-------|--------|---------|------|
| In-band emissions       | F = FO ± 2 MHz               | —     | —37.90 | —dBM    |      |
|                         | F = FO ± 3 MHz               | —     | —41.30 | —dBM    |      |
|                         | F = FO ± > 3 MHz             | —     | —42.80 | —dBM    |      |
| Modulation characteristics| Δ f₂ₐᵥ                    |       |        |         | kHz   |
|                          | Δ f₂ₘₐₓ                     |       |        |         | kHz   |
| Carrier frequency offset | |       |        |         | kHz    |
|                         | |       |        |         |        |
| Carrier frequency drift | |       |        |         | kHz    |

---

**Subtitle: 7.2.2 Bluetooth LE RF Receiver (RX) Characteristics**

---

### Table 7-12. Bluetooth LE - Receiver Characteristics - 1 Mbps

| Parameter                | Description                   | Min   | Typ    | Max     | Unit |
|--------------------------|-------------------------------|-------|--------|---------|------|
| Sensitivity @30.8% PER   | —                             |       |        |         | dBm  |
| Maximum received signal @30.8% PER | F = FO + 1 MHz               | -4    | -      | -       | dB   |
|                         | F = FO – 1 MHz               | -3    | -      | -       | dB   |
|                         | F = FO + 2 MHz               | -32   | -      | -       | dB   |
| Adjacent channel selectivity C/I | F = FO – 2 MHz               | -36   | -      | -       | dB   |
|                         | F ≥ FO + 3 MHz (1)           | —     |        |         |      |
|                         | F ≤ FO – 3 MHz              | -39   | -      | -       | dB   |
| Image frequency          | F = Fᵢₘₐgae + 1 MHz          | -38   | -      | -       | dB   |
| Adjacent channel to image frequency | F = Fᵢₘₑ₅₆ – 1 MHz         | -34   | -      | -       | dB   |
|                         |                             | —     |        |         |      |
| Out-of-band blocking performance | 2003 MHz ~ 2399 MHz          | -18   | -      | -       | dBm  |
|                         | 2484 MHz ~ 2997 MHz          | -16   | -      | -       | dBm  |
| Intermodulation         |                             | —     |        |         | dBm  |

---

**Footnote:**
1. Refer to the value of Adjacent channel to image frequency when F = Fᵢₘₑ₅₆ – 1 MHz.

---

**Footer:**  
Espressif Systems  
30  
ESP32-C3-MINI-1 & MINI-1U Datasheet v2.1

[Submit Documentation Feedback](#)