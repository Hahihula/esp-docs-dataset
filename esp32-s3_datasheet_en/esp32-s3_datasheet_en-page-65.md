**Title: Electrical Characteristics**

---

### Section Title

5.3 **VDD_SPI Output Characteristics**

#### Table Subtitle

Table 5-3. VDD_SPI Internal and Output Characteristics

| Parameter | Description | Typ | Unit |
|-----------|-------------|-----|------|
| R\_{SPI} | VDD_SPI powered by VDD3P3\_RTC via \(R_{SPI}\) for 3.3 V flash/PSRAM^2 | 14 | Ω |
| I\_{SPI} | Output current when VDD_SPI is powered by Flash Voltage Regulator for 1.8 V flash/PSRAM | 40 | mA |

**Footnotes:**
1. See in conjunction with Section 5.2. Power Scheme.
2. VDD3P3\_RTC must be more than \(VDD\_flash\_min + I\_flash\_max * R_{SPI}\);
   - \(\bullet\) \(VDD\_flash\_min\): minimum operating voltage of flash/PSRAM
   - \(\bullet\) \(I\_flash\_max\): maximum operating current of flash/PSRAM

---

### Section Title

5.4 **DC Characteristics (3.3 V, 25 °C)**

#### Table Subtitle

Table 5-4. DC Characteristics (3.3 V, 25 °C)

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| \(C_{IN}\) | Pin capacitance | — | 2 | — | pF |
| \(V_{IH}\) | High-level input voltage | \(\frac{0.75}{VDD^1}\) | V | -\(\frac{VDD^1 + 0.3}{V}\) | V |
| \(I_{IL}\) | Low-level input current | — | –0.3 | — | nA |
| \(I_{IH}\) | High-level input current | \(\frac{50}{V}\) | -\(\frac{25}{V}\) | 50 | nA |
| \(V_{OH}^2\) | High-level output voltage | \(\frac{0.8}{V}\) | V | — | V |
| \(I_{OL}^2\) | Low-level source current (VDD = 3.3 V, \(PA\_DRIVER = 3\)) | -40 | mA | — | mA |
| \(I_{OH}\) | High-level sink current (\(VDD = 3.3 V, PA\_DRIVER = 3\)) | \(\frac{28}{V}\) | mA | — | mA |
| \(R_{PU}\) | Internal weak pull-up resistor | -45 | kΩ | — | kΩ |
| \(R_{PD}\) | Internal weak pull-down resistor | -45 | kΩ | — | kΩ |
| \(V_{IH\_nRST}\) | Chip reset release voltage (CHIP\_PU voltage is within the specified range) | \(\frac{0.75}{VDD^1}\) | V | -\(\frac{VDD^1 + 0.3}{V}\) | V |
| \(I_{IL\_nRST}\) | Chip reset voltage (CHIP\_PU voltage is within the specified range) | — | –0.3 | \(-\frac{25}{V}\) | V |

**Footnotes:**
1. VDD = voltage from a power pin of respective power domain.
2. \(V_{OH}\) and \(V_{OL}\) are measured using high-impedance load.

---

**Footer**

Espressif Systems  
ESP32-S3 Series Datasheet v2.1

Submit Documentation Feedback