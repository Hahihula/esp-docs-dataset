**Title: RF Characteristics**

---

### Table 6-11: Transmitter Characteristics - Bluetooth LE 500 Kbps

| Parameter                  | Description                                    | Min   | Typ  | Max   | Unit |
|----------------------------|-----------------------------------------------|-------|------|-------|------|
| **RF transmit power**      | RF power control range                        | −24.00 | 0    | 20.00 | dBm  |
|                            | Gain control step                              |       | 3.00 | —     | dB   |
| **Carrier frequency offset and drift** | Max \( f_n \) for n=0,1,...k | Max \( f_0 - f_k \) | [\( f_n - f_{n-3} \)] | [\( f_0 - f_3 \)] | Δ \( f_{2\text{avg}} \) (for at least 99.9% of all Δ \( f_{2\text{max}} \)) | kHz |
|                            |                                                |       |      |       |      |
| **Modulation characteristics** | Min Δ \( f_2\text{max} \) | ± 2 MHz offset | ± 3 MHz offset | > ± 3 MHz offset | —    | dBm |
|                            |                                               |       |      |       |      |
| **In-band spurious emissions** | ± 2 MHz offset | ± 3 MHz offset | > ± 3 MHz offset | —     | —    |

---

### Section: Bluetooth LE RF Receiver (RX) Characteristics

---

#### Table 6-12: Receiver Characteristics - Bluetooth LE 1 Mbps

| Parameter                  | Description                                    | Min   | Typ  | Max   | Unit |
|----------------------------|-----------------------------------------------|-------|------|-------|------|
| **Sensitivity @30.8% PER** | —                                              |       |      |       | dBm  |
|                            | Maximum received signal @30.8% PER             |       | -97  | —     | dBm  |
| **Co-channel C/I**         | F = FO + 1 MHz                               |       | −3   | —     | dB   |
|                            | F = FO – 1 MHz                                |       | −4   | —     | dB   |
|                            | F = FO + 2 MHz                                |       | −29  | —     | dB   |
|                            | F = FO – 2 MHz                                |       | −31  | —     | dB   |
|                            | F = FO + 3 MHz                                |       | −33  | —     | dB   |
|                            | F = FO – 3 MHz                                |       | −27  | —     | dB   |
|                            | F ≥ FO + 4 MHz                                |       | −29  | —     | dB   |
| **F ≤ FO – 4 MHz**         | —                                              |       | -38  | —     | dB   |
| **Image frequency**        | —                                              |       |      |      |      |
|                            | F = F_{image} + 1 MHz                         |       | −41  | —     | dB   |
|                            | F = F_{image} – 1 MHz                         |       | -33  | —     | dB   |
| **Adjacent channel to image frequency** | 30 MHz ~ 2000 MHz | 2003 MHz ~ 2399 MHz | 2484 MHz ~ 2997 MHz | 3000 MHz ~ 12.75 GHz | —     | dBm |
| **Out-of-band blocking performance** | -15 dBm | -5 dBm | -5 dBm | -30 dBm | —    |

---

*Espressif Systems*
63
ESP32-C3 Series Datasheet v2.2

Submit Documentation Feedback