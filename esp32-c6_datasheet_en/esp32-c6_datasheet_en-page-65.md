**Title: Electrical Characteristics**

---

### Section Title

5.3 **VDD_SPI Output Characteristics**

#### Table Description (Table 5-3)

| Parameter | Description | Typ | Unit |
|-----------|-------------|-----|------|
| R\_{SPI} | VDD\_SPI powered by VDDPST2 via R\_{SPI} for 3.3 V flash | Ω | - |
| Note: See in conjunction with Section **2.5.2 Power Scheme**. | <br> VDD3P3\_RTC must be more than VDD\_flash\_min + I\_flash\_max \* R\_{SPI}; where<br>- VDD\_flash\_min = minimum operating voltage of flash<br>- I\_flash\_max = maximum operating current of flash | - | - |

---

### Section Title

5.4 **DC Characteristics (3.3 V, 25 °C)**

#### Table Description (Table 5-4)

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| C\_{IN} | Pin capacitance | - | pF | - | - |
| V\_{IH} | High-level input voltage | <0.75 \* VDD^1> | V | 0.25 \* VDD^1 + 0.3 | V |
| V\_{IL} | Low-level input voltage | -0.3 | V | 0.25 \* VDD^1 | V |
| I\_{IH} | High-level input current | nA | mA | <br> 50 | nA |
| I\_{IL} | Low-level input current | nA | mA | - | nA |
| V\_{OH}^2 | High-level output voltage | >0.8 \* VDD^1 | V | - | V |
| V\_{OL}^2 | Low-level output voltage | <br> 0.1 \* VDD^1 | V | - | V |
| I\_{OH} | High-level source current (VDD^1 = 3.3 V, V\_OH > 2.64 V, PAD\_DRIVER = 3) | mA | mA | <br> 40 | mA |
| I\_{OL} | Low-level sink current (VDD^1 = 3.3 V, V\_OL = 0.495 V, PAD\_DRIVER = 3) | mA | mA | - | mA |
| R\_{PU} | Internal weak pull-up resistor | kΩ | Ω | <br> 45 | kΩ |
| R\_{PD} | Internal weak pull-down resistor | kΩ | Ω | <br> 45 | kΩ |
| V\_{IH\_nRST} | Chip reset release voltage (CHIP\_PU voltage is within the specified range) | V | - | <br> 0.75 \* VDD^1 + 0.3 | V |
| V\_{IL\_nRST} | Chip reset voltage (CHIP\_PU voltage is within the specified range) | V | - | <br> 0.25 \* VDD^1 | V |

#### Footnotes
1. VDD = voltage from a power pin of respective power domain.
2. V\_{OH} and V\_{OL} are measured using high-impedance load.

---

### Section Title

5.5 **ADC Characteristics**

The measurements in this section are taken with an external 100 nF capacitor connected to the ADC, using DC signals as input, and at an ambient temperature of 25 °C with disabled Wi-Fi.
  
---

**Footer:**
Espressif Systems
ESP32-C6 Series Datasheet v1.4

Submit Documentation Feedback