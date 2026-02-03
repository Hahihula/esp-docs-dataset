**Title: Electrical Characteristics**

---

### Parameter Table

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| RF power control range | — | -12 | — | +9 | dBm |
| +20 dB bandwidth |  | F = FO ± 2 MHz | –47 | — | dBm |
| Adjacent channel transmit power | F = FO ± 3 MHz | –55 | — | dBm |
| Δ f₁ₐᵥₕ | F = FO ± > 3 MHz | -60 | — | — | dBm |
| Δ f₂ₘₐₓ |  | 133.7 | — | +9 | kHz |
| Δ f₂ₐᵥₕ/Δ f₁ₐᵥₕ | ICFT | –7 | — | — | kHz |
| Drift rate (DH1) |  | -0.7 | kHZ/50 µs |—— | —— |
| Drift (DH5) |  | +6 | — | — | kHz |

**Note:** There are in total eight power levels from level 0 to level 7, with transmit power ranging from –12 dBm to 9 dBm. When the power level rises by 1, the transmit power increases by 3 dB. Power level 4 is used by default and the corresponding transmit power is 0 dBm.

---

**Subtitle: 5.7.3 Receiver - Enhanced Data Rate**

### Table

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| Sensitivity @0.01% BER (π/4 DQPSK) | — | –90 | 89 | +88 | dBm |
| Maximum received signal @0.01% BER Co-channel C/I | F = FO ± 1 MHz | -7 | — | — | dB |
| Adjacent channel selectivity C/I (π/4 DQPSK) | Sensitivity @0.01% BER, Maximum received signal @0.01% BER; C/I c-channel: F = FO + 1 MHz | –25 | -35 |—— | —— |
| Adjacent channel selectivity C/I (8DPSK) | Sensitivity @0.01% BER, Maximum received signal @0.01% BER; C/I c-channel: F = FO ± 1 MHz | +7 | –45 |—— | —— |

---

**Subtitle: 5.7.4 Transmitter - Enhanced Data Rate**

Espressif Systems  
Submit Documentation Feedback

ESP32 Series Datasheet v5.2