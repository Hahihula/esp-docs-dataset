**Title: Boot Configurations**

---

### Table 4-2. Description of Timing Parameters for the Strapping Pins

| Parameter | Description                                                                                   | Min (ms) |
|-----------|--------------------------------------------------------------------------------------------------|----------|
| \( t_{SU} \) | Setup time is the time reserved for the power rails to stabilize before the CHIP_PU pin is pulled high to activate the chip. | 0        |
|            | Hold time is the time reserved for the chip to read the strapping pin values after CHIP_PU is already high and before these pins start operating as regular IO pins. |           |

---

**Figure Caption:**
- Figure 4-1. Visualization of Timing Parameters for the Strapping Pins

---

### Section Title:
#### 4.1 Chip Boot Mode Control

GP100 and GPIO46 control the boot mode after the reset is released. See Table 4-3 Chip Boot Mode Control.

---

**Table Caption:**
- Table 4-3. Chip Boot Mode Control

| Boot Mode | GPI00 | GPI046 |
|-----------|-------|--------|
| SPI boot mode | 1     | Any value |
| Joint download boot mode | 2    | 0       |

**Note:** 
- Bold marks the default value and configuration.
- Joint Download Boot mode supports the following download methods:
  - USB-OTG Download Boot
  - UART Download Boot
  - SPI Download Boot

---

### Section Title:
#### 4.2 VDD_SPI Voltage Control

Depending on the value of EFUSE_VDD_SPIFORCE, the voltage can be controlled in two ways.

---

**Footer:**
- Espressif Systems
- ESP32-S2-SOLO-2 & SOLO-2U Datasheet v1.3
- Submit Documentation Feedback