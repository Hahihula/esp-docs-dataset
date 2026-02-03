**Title: Electrical Characteristics**

---

### Subtitle: Work Mode

- **Table:** 
  | Min Typ | Max Unit |
  |---------|----------|
  | Transmit BT/BLE, POUT = 0 dBm | — mA |
  | Receive BT/BLE | 95 ~ 100 mA |

---

#### Section Title: Reliability (5.5)

**Subtitle:** Table 5-5. Reliability Qualifications

| Test Item | Test Conditions | Test Standard |
|-----------|-----------------|--------------|
| HTOL (High Temperature Operating Life) | 125 °C, 1000 hours | JESD22-A108 |
| ESD (Electro-Static Discharge Sensitivity) | HBM (Human Body Mode)^1 ± 2000 V CDM (Charge Device Mode)^2 ± 500 V | JS-001, JS-002 |
| Latch up | Current trigger ± 200 mA | JESD78 |
| Preconditioning | Voltage trigger 1.5 x VDD_max Bake 24 hours @125 °C Moisture soak (level 3: 192 hours @30 °C, 60% RH) IR reflow solder: 260 + 0 ° C, 20 seconds, three times | J-STD-020, JESD47, JESD22-A113 |
| TCT (Temperature Cycling Test) | —65 °C / 150 °C, 500 cycles | JESD22-A104 |
| Autoclave Test | 121 °C, 100% RH, 96 hours | JESD22-A102 |
| uHAST (Highly Accelerated Stress Test, unbiased) | 130 °C, 85% RH, 96 hours | JESD22-A118 |
| HTSL (High Temperature Storage Life) | 150 °C, 1000 hours | JESD22-A103 |

**Footnotes:**
1. JEDEC document JEP155 states that 500 V HBM allows safe manufacturing with a standard ESD control process.
2. JEDEC document JEP157 states that 250 V CDM allows safe manufacturing with a standard ESD control process.

---

#### Section Title: Wi-Fi Radio (5.6)

**Subtitle:** Table 5-6. Wi-Fi Radio Characteristics

| Parameter | Description | Min Typ | Max Unit |
|-----------|-------------|---------|----------|
| Operating frequency range note1 | — | 2412 | 2484 MHz |
| Output impedance note2 | - | Note 2 | Ω |
| TX power note3 | 11n, MCS7 mode (1b, 1 Mbps) | 18.5 | 98 dBm |
| | — | — | — |
| | 11b, 6 Mbps | −88 | — dBm |
| | 11g, 54 Mbps | −75 | — dBm |

**Footnotes:**
- Note 2 refers to the output impedance.
- Note 3 indicates that different modes have varying power requirements.

---

**Footer:** Espressif Systems  
Submit Documentation Feedback

ESP32 Series Datasheet v5.2