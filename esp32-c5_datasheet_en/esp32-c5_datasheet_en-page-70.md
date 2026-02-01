**Title: Electrical Characteristics**

---

### Subtitle: Current Consumption in Other Modes

#### Section Title: Table 5-11. Current Consumption in Modem-sleep Mode

| **Mode** | CPU Frequency (MHz) | Description | All Peripherals Typ (mA) | All Peripherals Clocks Disabled/Enabled |
|----------|----------------------|-------------|---------------------------|-----------------------------------------|
|          |                      |             |                          |                                          |
| 240      | WAITI                | CPU while loop | 18                        | 27                                      |
|          |                      | Run CoreMark   | 26                        | 35                                      |
|          |                      | WAITI         | 34                        | 43                                      |
| 160      |                      | CPU while loop | 15                        | 27                                      |
| Modem-sleep^2,3 | Run CoreMark   | CPU while loop | 20                        | 32                                      |
|          |                      | WAITI         | 26                        | 37                                      |
|          |                      | WAITI         | 12                        | 24                                      |
| 80       |                      | CPU while loop | 15                        | 26                                      |
| Modem-sleep^2,3 | Run CoreMark   | CPU while loop | 18                        | 29                                      |
|          |                      | WAITI         | 8                         | 18                                      |
| 40       |                      | CPU while loop | 10                        | 19                                      |
| Modem-sleep^2,3 | Run CoreMark   | CPU while loop | 12                        | 21                                      |

**Footnotes:**
1. In practice, the current consumption might be different depending on which peripherals are enabled.
2. In Modem-sleep mode, Wi-Fi is clock gated.
3. In Modem-sleep mode, the consumption might be higher when accessing flash.

---

### Subtitle: Current Consumption in Low-Power Modes

#### Section Title: Table 5-12. Current Consumption in Low-Power Modes

| **Mode** | Description | Typ (mA) |
|----------|-------------|----------|
| Light-sleep | CPU and wireless communication modules are powered down, peripheral clocks are disabled, and all GPIOs are high-impedance. CPU, wireless communication modules and peripherals are powered down, and all GPIOs are high-impedance | 0.25 |
| Deep-sleep | RTC timer and LP memory are powered on | 0.012 |
| Power off | CHIP_PU is set to low level; the chip is powered off | 0.002 |

---

### Subtitle: Reliability

#### Section Title: Table 5-13. Reliability Qualifications

| **Test Item** | **Test Conditions** | **Test Standard** |
|---------------|---------------------|--------------------|
| HTOL (High Temperature Operating Life) | 125 °C, 1000 hours, 3.6 V^1 | JESD22-A108 |
| ESD (Electro-Static Human Body Mode)^2 ± 2000 V | HBM (Human Body Mode)^2 ± 2000 V | JS-001 |
| Discharge Sensitivity | CDM (Charge Device Mode)^3 ± 1000 V | JS-002 |
| Latch up | Current trigger ± 200 mA | JESD78 |

**Footnotes:**
^1
^2
^3

---

**Footer:** Espressif Systems, ESP32-C5 Series Datasheet v1.0 Submit Documentation Feedback