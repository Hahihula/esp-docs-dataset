**Title: Electrical Characteristics**

---

### Section Title

#### Subsection Heading (5.6.2)

##### Current Consumption in Other Modes

###### Table Caption:
- **Table 5-8**: Current Consumption in Modem-sleep Mode

| Mode | CPU Frequency (MHz) | Description | All Peripherals Clocks Disabled (mA) | Typ All Peripherals Clocks Enabled (mA) |
|------|---------------------|-------------|---------------------------------------|-----------------------------------------|
|      |                     |             |                                       |                                          |
| Modem-sleep 2,3 |                   | CPU is running                          | 16                                     | 28                                      |
|                  |                    | CPU is idle                              | 17                                     | 21                                      |
|                  |                    | CPU is running                          | 13                                     | 18                                      |

##### Notes:
1. In practice, the current consumption might be different depending on which peripherals are enabled.
2. In Modem-sleep mode, Wi-Fi is clock gated.

###### Table Caption: 
- **Table 5-9**: Current Consumption in Low-Power Modes

| Mode | Description | Typ (µA) |
|------|-------------|----------|
| Light-sleep | VDD_SPI and Wi-Fi are powered down, and all GPIOs are high-impedance | 130      |
| Deep-sleep | RTC timer + RTC memory | 5        |
| Power off | CHIP_EN is set to low level, the chip is powered off | 1        |

---

#### Subsection Heading (5.7)

##### Memory Specifications

The data below is sourced from the memory vendor datasheet. These values are guaranteed through design and/or characterization but are not fully tested in production. Devices are shipped with the memory erased.

---

#### Subsection Heading (5.8)

##### Reliability

###### Table Caption:
- **Table 5-10**: Reliability Qualifications

| Test Item | Test Conditions | Test Standard |
|-----------|-----------------|---------------|
| HTOL (High Temperature Operating Life) | 125 °C, 1000 hours | JESD22-A108   |
| ESD (Electro-Static Human Body Mode) | HBM ± 2000 V | JS-001        |
| Discharge Sensitivity | CDM (Charge Device Mode) ± 1000 V | JS-002       |
| Latch up | Current trigger ± 200 mA | JESD78      |
| Voltage trigger | 1.5 x VDDmax |                |
| Preconditioning | Bag 24 hours @125 °C, Moisture soak (level 3: 192 hours @30 °C; 60% RH), IR reflow solder: 260 + 0 °C, 20 seconds, three times | J-STD-020, JESD47, JESD22-A113 |

---

**Footer**: Espressif Systems ESP32-C3 Series Datasheet v2.2

**Navigation**: Submit Documentation Feedback