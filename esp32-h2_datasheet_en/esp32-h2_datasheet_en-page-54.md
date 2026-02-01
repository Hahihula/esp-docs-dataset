**Title: Electrical Characteristics**

---

### Table 5-3 – cont’d from previous page

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| \( V_{OH}^2 \) | High-level output voltage | — | 0.8 × VDD¹ | — | V |
| \( V_{OL}^2 \) | Low-level output voltage | — | — | 0.1 × VDD¹ | V |
| \( I_{OH} \) | High-level source current (VDD¹ = 3.3 V, \( PAD\_DRIVER = 3\) ) | ≥ 2.64 V, PA | — | 40 | mA |
| \( I_{OL} \) | Low-level sink current (VDD¹ = 3.3 V, \( V_{OH}^2 = 0.495 \) V, PAD\_DRIVER = 3) ) | ≥ 3.3 V, PA | — | 28 | mA |
| \( R_{PU} \) | Internal weak pull-up resistor | — | - | 45 | kΩ |
| \( R_{PD} \) | Internal weak pull-down resistor | — | - | 45 | kΩ |
| \( V_{IH\_nRST} \) | Chip reset release voltage (CHIP_EN voltage is within the specified range) | ≥ 0.75 × VDD¹ | — | V | VDD¹ + 0.3 |
| \( V_{IL\_nRST} \) | Chip reset voltage (CHIP_EN voltage is within the specified range) | -0.3 | — | 0.25 × VDD¹ | V |

**Footnotes:**
1. VDD – voltage from a power pin of respective power domain.
2. \( V_{OH}^2 \) and \( V_{OL}^2 \) are measured using high-impedance load.

---

### 5.4 ADC Characteristics

The measurements in this section are taken with an external nF capacitor connected to the ADC, using DC signals as input, 3.3 V voltage, at ambient temperature of 25 °C and disabled modem.

---

**Table 5-4. ADC Characteristics**

| Symbol | Min | Max | Unit |
|--------|-----|-----|------|
| DNL (Differential nonlinearity)¹ | -8 | 12 | LSB |
| INL (Integral nonlinearity) | -10 | 10 | LSB |
| Sampling rate | — | 100 | kSPS² |

**Footnotes:**
1. To get better DNL results, you can sample multiple times and apply a filter, or calculate the average value.
2. kSPS means kilo samples-per-second.

---

The calibrated ADC results after hardware calibration and software calibration are shown in Table 5-5. For higher accuracy, you may implement your own calibration methods.

---

**Table 5-5. ADC Calibration Results**

| Parameter | Description | Min | Max | Unit |
|-----------|-------------|-----|-----|------|
| ATTN0, effective measurement range of \( O \sim 1000\) | — | -7 | 7 | mV |
| ATTN1, effective measurement range of \( O \sim 1300\) | — | -8 | 8 | mV |
| Total error | <details>—</details> | — | — | — |
| ATTN2, effective measurement range of \( O \sim 1900\) | — | -12 | 12 | mV |
| ATTN3, effective measurement range of \( O \sim 3300\) | — | -23 | 23 | mV |

---

**Footer:**
Espressif Systems  
54  
ESP32-H2 Series Datasheet v1.2

Submit Documentation Feedback