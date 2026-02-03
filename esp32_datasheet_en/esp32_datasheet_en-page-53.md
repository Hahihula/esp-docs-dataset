**Title: Electrical Characteristics**

---

### Subtitle: DC Characteristics (3.3 V, 25 °C)

#### Table Title:
Table 5-3. DC Characteristics (3.3 V, 25 °C)

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| \( C_{IN} \) | Pin capacitance | — | 0.75 × VDD¹ | pF | - |
| \( V_{IH} \) | High-level input voltage | – | (VDD¹ + 0.3) V | V | - |
| \( V_{IL} \) | Low-level input voltage | −0.3 | — | 0.25 × VDD¹ | V | - |
| \( I_{IH} \) | High-level input current | – | (VDD¹ = 3.3 V, power domain¹,²) | 50 nA | mA |
| \( I_{IL} \) | Low-level input current | — | — | 50 nA | - |
| \( V_{OH} \) | High-level output voltage | – | (VDD¹ = 3.3 V, power domain¹,²) | V | - |
| \( V_{OL} \) | Low-level output voltage | − | (VDD¹ = 0.8 × VDD¹) V | — | V |
| **High-level source current** | High-level source current (power domain¹,²) | – | <sup>VDD3P3_CPU</sup> power domain¹,² | 40 mA | - |
| \( I_{OH} \) | Output drive strength set to the maximum | — | VDD³P3_RTC power domain¹,² | (VDD¹ = 2.64 V, power domain¹,²) | mA |
| **Low-level sink current** | Low-level sink current (power domain¹,³) | – | <sup>VDD_SDIO</sup> power domain¹,³ | — | mA |
| \( I_{OL} \) | Output drive strength set to the maximum | 0.495 V | (VDD¹ = 3.3 V, VODL = 28 mA) | mA | - |
| **Resistance of internal pull-up resistor** | Resistance of internal pull-up resistor | — | <sup>RPu</sup> | kΩ | - |
| \( R_{PD} \) | Resistance of internal pull-down resistor | (VDD¹ = VDD³P3_RTC power domain¹,²) 45 mA | 0.75 × VDD¹ + 0.3 V | — | V |
| **Chip reset release voltage** | Chip reset release voltage (CHIP PU voltage is within the specified range) | <sup>RPu</sup> | CHIP PU voltage is within the specified range | 45 kΩ | - |

1. Please see Table IO_MUX for I/O domain's power domain of pins.
2. For VDD3P3_CPU and VDD3P3_RTC power domains, per-pin current sourced in the same domain is gradually reduced from around 40 mA to about 29 mA; \(V_{OH} = >2.64\) V as the number of current-source pins increases.
3. For VDD_SDIO power domain, per-pin current sourced in the same domain is gradually reduced from around 30 mA to around 10 mA.

---

### Subtitle: RF Current Consumption in Active Mode

The text describes that:
- The measurements are taken with a 3.3 V supply at 25 °C of ambient temperature.
- All transmitters' measures are based on a 50% duty cycle.

#### Table Title (Table 5-4):
Current Consumption Depending on RF Modes

| Work Mode | Min | Typ | Max | Unit |
|-----------|-----|-----|-----|------|
| Transmit 802.11b, DSSS 1 Mbps, POUT = +19.5 dBm | — | <sup>240</sup> | mA | - |
| Transmit 802.11g, OFDM 54 Mbps, POUT = +16 dBm | — | <sup>190</sup> | mA | - |
| Transmit 802.11n, OFDM MCS7, POUT = +14 dBm | — | <sup>180</sup> | mA | - |
| Receive 802.11b/g/n | (95 ~ 100) | mA | — | - |

---

**Footer:**
Espressif Systems
ESP32 Series Datasheet v5.2

Submit Documentation Feedback