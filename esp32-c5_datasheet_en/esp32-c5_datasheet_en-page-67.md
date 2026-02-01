**Title: Electrical Characteristics**

---

### Section Title

5.3 VDD_SPI Output Characteristics

#### Table Description (Table 5-3)

| Parameter | Description | Typ | Unit |
|-----------|-------------|-----|------|
| R\_{SPI} | VDD\_SPI powered by VDDPST2 via R\_{SPI} for 3.3 V flash or PSRAM^1 | Ω | - |
| Note: | See in conjunction with Section **2.5.2 Power Scheme**. | | |
| Note: | VDD3P3\_RTC must be more than VDD\_flash\_min + I\_{flash}\_max \* R\_{SPI}; where <br>● VDD\_flash\_min – minimum operating voltage of flash <br>● I\_{flash}\_max – maximum operating current of flash | | |

---

### Section Title

5.4 DC Characteristics (3.3 V, 25 °C)

#### Table Description (Table 5-4)

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| C\_{IN} | Pin capacitance | – | 2 | – | pF |
| V\_{IH} | High-level input voltage | -0.75 \* VDD^1 | – | VDD^1 + 0.3 | V |
| V\_{IL} | Low-level input voltage | — | – | 0.25 \* VDD^1 | V |
| I\_{IH} | High-level input current | — | – | 50 | nA |
| I\_{IL} | Low-level input current | — | – | 50 | nA |
| V\_{OH}^2 | High-level output voltage | -0.8 \* VDD^1 | – | V | |
| V\_{OL}^2 | Low-level output voltage | — | – | 0.1 \* VDD^1 | V |
| I\_{OH} | High-level source current (VDD^1 = 3.3 V, V\_{OH} >= -2.64 V, PAD\_DRIVER = 3) | 40 | — | mA | |
| I\_{OL} | Low-level sink current (VDD^1 = 3.3 V, V\_{OL} = 0.495 V, PAD\_DRIVER = 3) | -28 | – | mA | |
| R\_{PU} | Internal weak pull-up resistor | — | 45 | kΩ | |
| R\_{PD} | Internal weak pull-down resistor | — | 45 | kΩ | |
| V\_{IH\_nRST} | Chip reset release voltage (CHIP\_PU voltage is within the specified range) | -0.75 \* VDD^1 | – | VDD^1 + 0.3 | V |
| V\_{IL\_nRST} | Chip reset voltage (CHIP\_PU voltage is within the specified range) | — | – | 0.25 \* VDD^1 | V |

---

**Footnotes:**
1. VDD – voltage from a power pin of a respective power domain.
2. V\_{OH} and V\_{OL} are measured using high-impedance load.

---

**Footer**

Espressif Systems  
ESP32-C5 Series Datasheet v1.0

Submit Documentation Feedback