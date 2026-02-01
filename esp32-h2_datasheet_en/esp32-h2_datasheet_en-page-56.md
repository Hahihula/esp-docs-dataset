**Title: Electrical Characteristics**

---

### Table 5-8 – cont’d from previous page

| Work mode | Frequency (MHz) | Description | Typ \(1\) (\(mA\)) | Typ \(1\) (\(mA\)) |
|-----------|------------------|-------------|--------------------|--------------------|
|           |                  | All Peripheral Clocks Disabled |                | All Peripheral Clocks enabled |
| 48        | CPU running      |                          | **7**              | **11**             |
|          | CPU in idle      |                          | **5**              | **9**              |
| 32        | CPU running      |                          | **4**              | **8**              |
|          | CPU in idle      |                          | **3**              | **7**              |

1. In practice, the current consumption might be different depending on which peripherals are enabled.
2. In Modem-sleep mode, the current consumption might be higher when accessing flash.

---

### Table 5-9. Current Consumption in Low-Power Modes

| Work mode    | Description                                                                                   | Typ (\(\mu\)A) |
|--------------|---------------------------------------------------------------------------------------------|----------------|
| Light-sleep  | CPU and wireless communication modules are powered down, peripheral clocks are disabled, and all GPIOs are high-impedance | **85**          |
|              | CPU, wireless communication modules and peripherals are powered down, and all GPIOs are high-impedance | **25**          |
| Deep-sleep   | LP timer and LP memory are powered on                                                        | **7**           |
| Power off    | CHIP_EN is set to low level, the chip is powered off                                        | **1**           |

---

### 5.6 Reliability

#### Table 5-10. Reliability Qualifications

| Test Item       | Test Conditions                                                                                   | Test Standard        |
|-----------------|--------------------------------------------------------------------------------------------------|----------------------|
| HTOL (High Temperature Operating Life) | 125 °C, 1000 hours                                                                               | JESD22-A108          |
| ESD (Electro-Static HBM (Human Body Mode)) \(1\) ± 2000 V                                      |                                                                                                   | JS-001               |
| Discharge Sensitivity | CDM (Charge Device Mode) \(2\) ± 1000 V                                                        | JS-002               |
| Latch up        | Current trigger ± 200 mA                                                                       | JESD78               |
|                 | Voltage trigger 1.5 x VDD\(_{max}\)                                                              |                      |
| Preconditioning | Bake 24 hours @125 °C                                                                           | J-STD-020, JESD47, IR reflow solder: 260 + 0 °C, 20 seconds, three times                       | JESD22-A113          |
|                 | Moisture soak (level 3: 192 hours @30 °C, 60% RH)                                              |                      |
| TCT (Temperature Cycling Test)                    | -65 °C / 150 °C, 500 cycles                                                                      | JESD22-A104          |
| uHAST (Highly Accelerated Stress Test, unbiased)   | 130 °C, 85% RH, 96 hours                                                                         | JESD22-A118          |

---

**Footer:**
Espressif Systems
ESP32-H2 Series Datasheet v1.2

Submit Documentation Feedback