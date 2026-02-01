**Title: ESP32-P4 Series Comparison**

---

### Section 1

#### Subsection Title: Nomenclature (1.1)

- **Diagram Description:** 
  - The diagram shows the nomenclature for an ESP32-P4 chip.
  - Labels include:
    - "ESP32-P4"
    - Letters indicating different parts of the pinout, such as 'N', 'R', 'W', and 'X'.
    - Connections to PSRAM size (MB), a 16-line PSRAM at 1.8 V voltage level.
    - Indications for PSRAM temperature with "Normal" specified by N: Normal temperature.

- **Figure Caption:** 
  Figure 1-1. ESP32-P4 Series Nomenclature

---

#### Subsection Title: Comparison (1.2)

**Table Description:**
- The table compares different ordering codes of the ESP32-P4 series.
  
| Ordering Code | In-Package PSRAM | Ambient Temp. (°C) | VDD_PS RAM_0/1 Voltage |
|---------------|------------------|--------------------|------------------------|
| ESP32-P4NRW16| 16 MB (OPI/HPI)^4| -40 ~ 85           | 1.8 V                  |
| ESP32-P4NRW32| 32 MB (OPI/HPI)^4| -40 ~ 85           | 1.8 V                  |

**Footnotes:**
1. For details on chip marking and packing, see Section 6 Packaging.
2. Ambient temperature specifies the recommended temperature range of the environment immediately outside an Espressif chip.
3. For more information on VDD_PS RAM_0/1, see Section 2.6 Power Supply.
4. OPI of PSRAM supports transferring eight-bit commands, addresses, and data; HPI supports transferring eight-bit commands and addresses as well as 16-bit data. For details about SPI modes, see Section 2.7 Pin Mapping Between Chip and Flash.

---

**Footer:**
- Page number: 12
- Document title: ESP32-P4 Series Datasheet v0.6

**Links:** 
- Submit Documentation Feedback