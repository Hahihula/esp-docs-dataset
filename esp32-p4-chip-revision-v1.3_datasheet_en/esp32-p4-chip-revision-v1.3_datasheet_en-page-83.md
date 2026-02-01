**Title: Electrical Characteristics**

---

### Table 5-7 – cont’d from previous page

| Frequency (MHz) | Description | Typ1 (mA) | Typ2 (mA) |
|------------------|-------------|-----------|-----------|
| **Work mode**    |             |           |           |
| WAITI            | Dual core in idle state | 32       | 59        |
|                 | Dual-core while(1) loop operation | 56      | 77        |
|                 | Single core running CoreMark instructions, the other core in idle state | 51     | 72        |
|                 | Dual core running 32-bit data access instructions | 65    | 87        |
| WAITI            | Dual core (idle state) | 28       | 44        |
|                 | Dual-core while(1) loop operation | 40      | 53        |
|                 | Single core running CoreMark instructions, the other core in idle state | 37     | 51        |
|                 | Dual core running 32-bit data access instructions | 45    | 61        |
| WAITI            | Dual core (idle state) | 26       | 35        |
|                 | Dual-core while(1) loop operation | 31      | 39        |
|                 | Single core running CoreMark instructions, the other core in idle state | 30     | 38        |
|                 | Dual core running 32-bit data access instructions | 33    | 41        |

**Footnotes:**
1. Current consumption when all peripheral clocks are disabled.
2. Current consumption when all peripheral clocks are enabled. In practice, the current consumption might be different depending on which peripherals are enabled.
3. In Active mode, the current consumption might be higher when accessing flash/PSRAM.

---

### Table 5-8 – Current Consumption in Low-Power Modes

| Mode       | Description | Typ1 (mA) |
|------------|-------------|-----------|
| Light-sleep2 | All GPIOs are high-impedance, and all power supplies are enabled. Most peripherals are disabled, and chip is connected through USB | 3.5        |
|             |            |           | 0.25      |
| Deep-sleep | LP timer and LP memory are powered on | 0.025     |
| Power off  | The power consumption data was measured with USB 2.0 not working, the current in Light-sleep mode refers to the current measured when the PSRAM is not powered ( increases by about 0.2 mA). In addition to the current required for the PSRAM’s operating mode. |           |

**Footnotes:**
1. The power consumption data was measured with USB 2.0, chip set at low level.
2. Current in Light-sleep mode refers when PSU is not powered.

---

*Espressif Systems*
*ESP32-P4 Series Datasheet v0.6*

[Submit Documentation Feedback](#)