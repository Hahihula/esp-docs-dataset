**Title: Boot Configurations**

---

### Table 3-2. Description of Timing Parameters for the Strapping Pins

| Parameter | Description                                                                                   | Min (ms) |
|-----------|--------------------------------------------------------------------------------------------------|----------|
| tSU       | Setup time is the time reserved for the power rails to stabilize before the CHIP_EN pin is pulled high to activate the chip. | 0        |
| tH        | Hold time is the time reserved for the chip to read the strapping pin values after CHIP_EN is already high and before these pins start operating as regular IO pins. | 3        |

**Figure Caption:**
- Figure 3-1. Visualization of Timing Parameters for the Strapping Pins

---

### Section Title:
#### Chip Boot Mode Control (Subsection)

GPI08 and GPIO9 control the boot mode after the reset is released.

See Table 3-3, Chip Boot Mode Control:

| Boot Mode | GPIO8    | GPIO9   |
|-----------|----------|---------|
| SPI Boot  | Any value| 1       |
| Joint Download Boot | Bold marks the default value and configuration. | 0 |

**Table Caption:**
- Table 3-3, Chip Boot Mode Control

Joint Download Boot mode supports the following download methods:
- USB Download Boot
  - USB-Serial-JTAG Download Boot
- UART Download Boot

---

**Footer Information:**  
Espressif Systems  
Submit Documentation Feedback  

**Page Number and Document Version:**
23  
ESP32-H2 Series Datasheet v1.2