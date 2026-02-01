**Title: Electrical Characteristics**

---

### Table 5-12 – PSRAM Specifications

| Parameter | Description                   | Min   | Typ    | Max     | Unit |
|-----------|-------------------------------|-------|--------|---------|------|
| VCC       | Power supply voltage (1.8 V)  | 1.62  | 1.80   | 1.98    | V    |
|           | Power supply voltage (3.3 V)  | 2.7   | 3.3    | 3.6     | V    |
| FC        | Maximum clock frequency       | 80    | —      | -      | MHz |

---

**Title: Reliability**

### Subtitle: Test Conditions

#### Table 5-13 – Reliability Qualifications

| Test Item         | Test Conditions                                                                                   | Test Standard            |
|-------------------|--------------------------------------------------------------------------------------------------|--------------------------|
| HTOL (High Temperature Operating Life) | 125 °C, 1000 hours                                                                                 | JESD22-A108              |
| ESD (Electro-Static Discharge Sensitivity) | HBM (Human Body Mode) ± 2000 V; CDM (Charge Device Mode) ± 1000 V                                | JS-001                   |
| Latch up          | Current trigger ± 200 mA                                                                         | JESD78                   |
| Preconditioning   | Voltage trigger 1.5 x VDD_max<br>Base: 24 hours @125 °C                                      | J-STD-020, JESED47,     |
|                   | Moisture soak (level 3: 192 hours @30 °C; 60% RH)                                              |                         |
| IR reflow solder | 260 + O °C for 2 seconds, three times                                                            | JESD22-A113              |
| TCT (Temperature Cycling Test)       | -65 °C / 150 °C, 500 cycles                                                                       | JESD22-A104              |
| uHAST (Highly Accelerated Stress Test, unbiased)      | 130 °C, 85% RH; 96 hours                                                                         | JESD22-A118              |
| HTSL (High Temperature Storage Life)   | 150 °C, 1000 hours                                                                                 | JESD22-A103              |
| LTSL (Low Temperature Storage Life)    | -40 °C, 1000 hours                                                                                 | JESD22-A119              |

---

Footnotes:
1. JEDEC document JEP155 states that 500 V HBM allows safe manufacturing with a standard ESD control process.
2. JEDEC document JEP157 states that 250 V CDM allows safe manufacturing with a standard ESD control process.

---

**Footer:**
Espressif Systems  
ESP32-S3 Series Datasheet v2.1

[Submit Documentation Feedback](#)