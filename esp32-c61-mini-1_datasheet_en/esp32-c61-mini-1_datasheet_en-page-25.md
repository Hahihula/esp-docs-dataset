**Title: Electrical Characteristics**

The values presented in this section are preliminary and may change with the final release of this datasheet.

---

**Subtitle: Absolute Maximum Ratings (Section 6.1)**

Stresses above those listed in Table **12 Absolute Maximum Ratings** may cause permanent damage to the device. These are stress ratings only, functional operation at these or any other conditions beyond what is indicated under Table **13 Recommended Operating Conditions** is not implied. Exposure to absolute-maximum-rated conditions for extended periods may affect device reliability.

- **Table 12: Absolute Maximum Ratings**
  - Symbol | Parameter | Min | Max | Unit
  - VDD33 | Power supply voltage | –0.3 | 3.6 | V

---

**Subtitle: Recommended Operating Conditions (Section 6.2)**

- **Table 13: Recommended Operating Conditions**

| Symbol | Parameter | Min | Typ | Max | Unit |
|--------|-----------|-----|-----|-----|------|
| VDD33 | Power supply voltage | 3.0 | — | 3.6 | V |
| IVDD | Current delivered by external power supply | 0.5 | — | — | A |
| TA | Operation ambient temperature | –40 | — | 85 | °C |

---

**Subtitle: DC Characteristics (Section 6.3) at **(3.3 V, 25°C)****

- **Table 14: DC Characteristics (3.3 V, 25°C)**

| Symbol | Parameter | Min | Typ | Max | Unit |
|--------|-----------|-----|-----|-----|------|
| CIN | Pin capacitance | — | 2 | — | pF |
| VIH | High-level input voltage | 0.75 × VDD1^1 | – | +0.3 | V |
| VIL | Low-level input voltage | −0.3 | - | 0.25 × VDD1^1 | V |
| IIL | High-level input current | — | 50 | nA |
| IL | Low-level input current | — | 50 | nA |
| VOH | High-level output voltage | 0.8 × VDD1^1 | – | - | V |
| VOL | Low-level output voltage | − | 0.1 × VDD1^1 | V |
| IOL | High-level source current (VDD1 = 3.3 V, VOH >= 2.64 V, PAD DRIVER = 3) | — | 40 | mA |
| IOL | Low-level sink current (VDD1 = 3.3 V, VOL = 0.495 V, PAD_DRIVER = 3) | – | 28 | mA |
| RPU | Pull-up resistor | − | 45 | — | kΩ |
| RPD | Pull-down resistor | − | 45 | — | kΩ |
| VIH_nRST | Chip reset release voltage | 0.75 × VDD1^1 | – | +0.3 | V |

---

**Footer:**
- Espresso Systems
- Page number: 25
- Document version: ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6

**Note:** The superscripted numbers (e.g., ^1) indicate references to other parts of the document, which are not provided in this text excerpt.

---

**Submit Documentation Feedback**

[Feedback link or button]