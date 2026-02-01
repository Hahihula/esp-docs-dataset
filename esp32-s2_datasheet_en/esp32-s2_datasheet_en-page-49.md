**Title: Electrical Characteristics**

---

### Subtitle: VDD_SPI Output Characteristics

#### Table Title:
Table 5-3. VDD_SPI Internal and Output Characteristics

| Parameter | Description | Typ | Unit |
|-----------|-------------|-----|------|
| R\_{SPI} | VDD_SPI powered by VDDP3\_RTC via \(R_{SPI}\) for 3.3 V flash/PSRAM^2 | 5 | Ω |
| I\_{SPI} | Output current when VDD\_SPI is powered by Flash Voltage Regulator for 1.8 V flash/PSRAM | 40 | mA |

**Footnotes:**
1. See in conjunction with Section **2.5.2 Power Scheme**.
2. VDD3P3\_RTC must be more than \(VDD\_flash\_min + I\_{flash\_max}\) \* 
   - Where:
     - \(VDD\_flash\_min\) – minimum operating voltage of flash/PSRAM
     - \(I\_{flash\_max}\) – maximum operating current of flash/PSRAM

---

### Subtitle: DC Characteristics (3.3 V, 25 °C)

#### Table Title:
Table 5-4. DC Characteristics (3.3 V, 25 °C)

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| \(C_{IN}\) | Pin capacitance^1 | – | 2 | — | pF |
| \(V_{IH}\) | High-level input voltage | \(\frac{0.75}{\text{VDD}}\) | V | \(\frac{\text{VDD} + 0.3}{\text{VDD}}\) | V |
| \(V_{IL}\) | Low-level input voltage | –0.3 | — | -0.25 × VDD^1 | V |
| \(I_{IH}\) | High-level input current | \(\frac{\text{VDD}}{4}\) | nA | 50 | nA |
| \(I_{IL}\) | Low-level input current | – | — | -50 | nA |
| \(V_{OH}^2\) | High-level output voltage | (0.8 × VDD)^1 | V | \(\frac{\text{VDD}}{4}\) | V |
| \(I_{OH}\) | Low-level source current (\(VDD = 3.3\), \(VOH ≥ 2.64\) V, PAD\_DRIVER = 3) | – | — | -40 | mA |
| \(I_{OL}\) | Low-level sink current (VDD^1 = 3.3 V, \(VO_{OL} = 0.495\) V, PAD\_DRIVER = 3) | \(\frac{28}{\text{VDD}}\) | mA | – | mA |
| \(R_{PU}\) | Internal weak pull-up resistor^1 | — | -45 | kΩ | kΩ |
| \(R_{PD}\) | Internal weak pull-down resistor^1 | 0.75 × VDD | \(\frac{\text{VDD} + 0.3}{\text{VDD}}\) | – | kΩ |
| \(V_{IH\_nRST}\) | Chip reset release voltage (CHIP\_PU voltage is within the specified range) | — | -0.25 × VDD^1 | \(\frac{\text{VDD} + 0.3}{\text{VDD}}\) | V |
| \(I_{IL\_nRST}\) | Chip reset voltage (CHIP\_PU voltage is within the specified range) | – | — | -0.25 × VDD^1 | V |

**Footnotes:**
1. \(\text{VDD} =\) voltage from a power pin of respective power domain.
2. \(VO_{OH}\) and \(VO_{OL}\) are measured using high-impedance load.

---

### Subtitle: ADC Characteristics

The measurements in this section are taken with an external 100 nF capacitor connected to the ADC, using DC signals as input, and at an ambient temperature of **25 °C** with disabled Wi-Fi. 

---

*Espressif Systems*

49
ESP32-S2 Series Datasheet v1.8

[Submit Documentation Feedback](#)