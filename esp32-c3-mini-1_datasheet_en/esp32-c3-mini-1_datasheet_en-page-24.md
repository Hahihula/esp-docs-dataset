**Title: Electrical Characteristics**

---

### Note:
The content below is excerpted from Section Power Consumption in Other Modes in ESP32-C3 Series Datasheet.

---

#### Subtitle 6.4.2 Current Consumption in Other Modes

##### Table Title (Table-6): Current Consumption in Modem-sleep Mode
| Mode | CPU Frequency (MHz) | Description | All Peripherals Clocks Disabled (mA) | All Peripherals Clocks Enabled (mA) |
|------|---------------------|-------------|---------------------------------------|--------------------------------------|
|      |                     | Typ         |                                       |                                      |
| 160  |                     | CPU is running | 23                                   | 28                                  |
| Modem-sleep | 2.3                | CPU is idle   | 16                                   | 21                                  |
|        |                     | CPU is running | 17                                   | 22                                  |
| 80    |                     | CPU is idle   | 13                                   | 18                                  |

##### Footnotes:
1. In practice, the current consumption might be different depending on which peripherals are enabled.
2. In Modem-sleep mode, Wi-Fi is clock gated.
3. In Modem-sleep mode, the consumption might be higher when accessing flash. For a flash rated at 80 Mbit/s, in SPI 2-line mode the consumption is 10 mA.

---

##### Table Title (Table-7): Current Consumption in Low-Power Modes
| Mode | Description | Typ (\(\mu\)A) |
|------|-------------|---------------|
| Light-sleep | VDD_SPI and Wi-Fi are powered down, and all GPIOs are high-impedance | 130           |
| Deep-sleep | RTC timer + RTC memory | 5             |
| Power off | CHIP_EN is set to low level, the chip is powered off | 1             |

---

#### Subtitle: Memory Specifications

The data below is sourced from the memory vendor datasheet. These values are guaranteed through design and/or characterization but are not fully tested in production. Devices are shipped with the memory erased.

##### Table Title (Table-8): Flash Specifications
| Parameter | Description | Min  | Typ   | Max  | Unit |
|-----------|-------------|------|-------|------|------|
| VCC       | Power supply voltage (1.8 V) | 1.65 | 1.80 | 2.00 | V    |
|           | Power supply voltage (3.3 V)   | 2.7  | 3.3  | 3.6  | V    |
| FC        | Maximum clock frequency         | —    | —    | MHz  |      |
| —         | Program/erase cycles            | 100,000 |     | cycles |      |
| T RET     | Data retention time              | 20   | years|       |      |
| T PP      | Program write time               | 0.8  | ms   |       |      |
| T SE      | Sector erase (4 KB)             | —    | 70   | 500  | ms   |
| T BE1     | Block erase (32 KB)             | —    | 0.2  | 2 s  |      |
| T BE2     | Block erase (64 KB)             | —    | 0.3  | 3 s  |      |

---

**Footer:**
Espressif Systems
Page number: 24

Submit Documentation Feedback ESP32-C3-MINI-1 & MINI-1U Datasheet v2.1