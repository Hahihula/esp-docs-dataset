**Title: Electrical Characteristics**

---

### Section Title

5.3 VDD_SPI Output Characteristics

#### Table Description (Table 5-3)

| Parameter | Description | Typ | Unit |
|-----------|-------------|-----|------|
| R\_{SPI} | VDD\_SPI powered by VDD3P3\_CPU via R\_{SPI} for 3.3 V flash\_CPU | Ω | - |

1. See in conjunction with Section **2.5.2 Power Scheme**.
2. VDD3P3\_CPU must be more than VDD\_flash\_min + I\_flash\_max \* R\_{SPI}; where
   - VDD\_flash\_min – minimum operating voltage of flash\_CPU
   - I\_flash\_max – maximum operating current of flash\_CPU

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
| V\_{OL}^2 | Low-level output voltage |—— | – | 0.1 \* VDD^1 | V |
| I\_{OH} | High-level source current (VDD^1 = 3.3 V, V\_OH > 2.64 V, PAD\_DRIVER = 3) | — | 40 | mA | |
| I\_{OL} | Low-level sink current (VDD^1 = 3.3 V, V\_OL = 0.495 V, PAD\_DRIVER = 3) | – | 28 | mA | |
| R\_{PU} | Internal weak pull-up resistor | — | 45 | kΩ | |
| R\_{PD} | Internal weak pull-down resistor |—— | 45 | kΩ | |
| V\_{IH\_nRST} | Chip reset release voltage (CHIP\_EN voltage is within the specified range) | – | - | VDD^1 + 0.3 | V |
| V\_{IL\_nRST} | Chip reset voltage (CHIP\_EN voltage is within the specified range) | — | – | 0.25 \* VDD^1 | V |

Footnotes:
1. VDD = voltage from a power pin of a respective power domain.
2. V\_{OH} and V\_{OL} are measured using high-impedance load.

---

**Footer**

Espressif Systems  
Page 55 ESP32-C3 Series Datasheet v2.2

Submit Documentation Feedback