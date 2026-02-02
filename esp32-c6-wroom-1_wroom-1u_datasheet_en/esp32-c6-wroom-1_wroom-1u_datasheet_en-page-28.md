**Title: Electrical Characteristics**

---

**Note:**  
The content below is excerpted from Section Current Consumption in Other Modes in ESP32-C6 Series Datasheet.

---

### 6.4.2 Current Consumption in Other Modes

#### Table 6-7. Current Consumption in Modem-sleep Mode
| Mode | CPU Frequency (MHz) | Description | All Peripherals Clocks Disabled Typ (mA) | All Peripherals Clocks Enabled Typ (mA) |
|------|---------------------|-------------|-----------------------------------------|----------------------------------------|
|      |                     |             |                                         |                                        |
| Modem-sleep 2,3 | 160                 | CPU is running                             | 27                                     | 38                                    |
|                  |                     | CPU is idle                                | 17                                     | 28                                    |
|                  |                     | CPU is running                            | 19                                     | 30                                    |
|                  |                     | CPU is idle                                | 14                                     | 25                                    |

**Footnotes:**
1. In practice, the current consumption might be different depending on which peripherals are enabled.
2. In Modem-sleep mode, Wi-Fi is clock gated.
3. In Modem-sleep mode, the consumption might be higher when accessing flash.

---

#### Table 6-8. Current Consumption in Low-Power Modes
| Mode | Description | Typ (µA) |
|------|-------------|----------|
| Light-sleep | CPU and wireless communication modules are powered down, peripheral clocks are disabled, and all GPIOs are high-impedance | 180 |
| Deep-sleep | RTC timer and LP memory are powered on | 7 |
| Power off | CHIP_PU is set to low level, the chip is powered off | 1 |

---

### 6.5 Memory Specifications

The data below is sourced from the memory vendor datasheet. These values are guaranteed through design and/or characterization but are not fully tested in production. Devices are shipped with the memory erased.

#### Table 6-9. Flash Specifications
| Parameter | Description | Min Typ (V) | Max Typ (V) | Unit |
|-----------|-------------|--------------|-------------|------|
| VCC       | Power supply voltage (1.8 V) | — | 2.00 | V |
|           | Power supply voltage (3.3 V) | 1.65 | 1.80 |   |
| FC        | Maximum clock frequency | 2.7 | 3.3 | MHz |
|           | Program/erase cycles | — | ∞ | cycles |
| T RET     | Data retention time | 100,000 | — | years |
| T PP      | Page program time | 20 | 0.8 | ms |

---

**Footer:**  
Espressif Systems  
ESP32-C6-WROOM-1 & WROOM-1U Datasheet v1.4

Submit Documentation Feedback