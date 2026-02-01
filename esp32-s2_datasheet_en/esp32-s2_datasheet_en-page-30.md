**Title: Boot Configurations**

---

### Table 3-2. Description of Timing Parameters for the Strapping Pins

| Parameter | Description                                                                                   | Min (ms) |
|-----------|--------------------------------------------------------------------------------------------------|----------|
| t_SU      | Setup time is the time reserved for the power rails to stabilize before the CHIP_PU pin is pulled high to activate the chip. | 0        |
|           |                                                                                                 |          |
| t_H       | Hold time is the time reserved for the chip to read the strapping pin values after CHIP_PU is already high and before these pins start operating as regular IO pins. | 3        |

---

**Figure Caption:**
- Figure 3-1. Visualization of Timing Parameters for the Strapping Pins

---

### Section Title:
#### 3.1 Chip Boot Mode Control
GPI00 and GPIO46 control the boot mode after the reset is released. See Table 3-3 Chip Boot Mode Control.

---

**Table Caption:**
- Table 3-3. Chip Boot Mode Control

| Boot Mode | GPI00    | GPIO46   |
|-----------|----------|----------|
| SPI boot mode | 1        | Any value |
| Joint download boot mode | Bold marks the default value and configuration. | 2 |

**Note:**
Joint Download Boot mode supports the following download methods:
- USB-OTG Download Boot
- UART Download Boot
- SPI Download Boot

---

### Section Title:
#### 3.2 VDD_SPI Voltage Control
The required VDD_SPI voltage for the chips of the ESP32-S2 Series can be found in Table 1-1 ESP32-S2 Series Comparison.

Depending on the value of EFUSE_VDD_SPI FORCE, the voltage can be controlled in two ways.
Espressif Systems

---

**Footer:**
- Page number and document information
- Submit Documentation Feedback