**Title:**
2 Pins

---

**Table Title:** Table 2-12. Voltage Regulators

| Voltage Regulator | Output | Power Supply |
|-------------------|--------|--------------|
| HP LDO           | 1.1 V  | HP power domain |
| LP LDO           | 1.1 V  | LP power domain |
| Flash LDO        | 1.8 V/3.3 V | Can be configured to power off-package flash |
| VDD_PSRAM LDO    | 1.9 V  | Can be configured to power in-package PSRAM |
| VO3 LDO          | 0.5 ~ 2.7 V/3.3 V | Can be configured to power external devices |
| VO4 LDO          | 0.5 ~ 2.7 V/3.3 V | Can be configured to power external devices |

---

**Figure Title:** Figure 2-2. ESP32-P4 Power Scheme

---

**Subtitle:**
2.6.3 Chip Power-up and Reset

**Body Text:**
Once the power is supplied to the chip, its power rails need a short time to stabilize. After that, CHIP_PU – the pin used for power-up and reset – is pulled high to activate the chip. For information on CHIP_PU as well as power-up and reset timing, see Figure 2-3 and Table 2-13.

---

**Figure Title:** Figure 2-3. Visualization of Timing Parameters for Power-up and Reset

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32-P4 Series Datasheet v0.6