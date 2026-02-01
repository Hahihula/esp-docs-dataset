**Title: Electrical Characteristics**

---

### Table of Contents

- **Table 5-2 – cont'd from previous page**
- **Section 5.3 VDDO_FLASH Output Characteristics**
- **Section 5.4 DC Characteristics (3.3 V, 25 °C)**

---

#### Section Breakdowns and Tables:

**1. Table 5-2 - continued**

| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| **VDD_MIPI_DPHY** | Recommended input voltage | — | V | 2.75 | V |
| **VDD_USBPHY** | Recommended input voltage | -40 | A | 85 | °C |

- Note: The chip can automatically adjust the input voltage of VDD_HP_x based on the situation.

---

#### Section Breakdowns:

**Section 5.3 VDDO_FLASH Output Characteristics**

- **Table 5-3**: VDDO_FLASH Internal and Output Characteristics

| Parameter Description | Typ | Unit |
|------------------------|-----|------|
| \( R_{VFB} \) for 3.3 V flash^1 | Ω |
| Output current when VDDO_FLASH is powered by Flash Voltage Regulator (for 1.8 V flash) | mA |

- Note: 
  - See in conjunction with Section **2.6.2 Power Scheme**.
  - \( R_{VFB} \): must be more than the minimum operating voltage of flash (\( VDD\_flash\_min \)) plus maximum current (I_flash_max).

---

**Section Breakdowns and Tables:**

**Section 5.4 DC Characteristics (3.3 V, 25 °C)**

- **Table 5-4**: DC Characteristics at specified conditions.

| Parameter Description | Min | Typ | Max | Unit |
|------------------------|-----|-----|-----|------|
| \( C_{IN} \) | Pin capacitance | — | pF |
| \( V_{IH} \) | High-level input voltage | 0.75 x VDD^1 | V |
| \( I_{IL} \) | Low-level current (VDD^1 = 3.3 V, VOH > 2.64 V, PAD_DRIVER = 3) | — | mA |
| \( R_{PU} \) | Pull-up resistor | 0.8 x VDD^1 | kΩ |
| \( I_{OL} \) | Low-level sink current (VDD^1 = 3.3 V, VOH = 0.495 V, PAD_DRV = 3) | — | mA |
| \( R_{PD} \) | Pull-down resistor | - | kΩ |

---

**Footer:**

Espressif Systems  
Submit Documentation Feedback

ESP32-P4 Series Datasheet v0.6