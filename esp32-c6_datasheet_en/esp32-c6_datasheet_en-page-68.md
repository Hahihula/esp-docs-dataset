Title: Electrical Characteristics

---

**Table 5-11. Current Consumption in Low-Power Modes**

| Mode       | Description                                                                                   | Typ (µA) |
|------------|----------------------------------------------------------------------------------------------|----------|
| Light-sleep| CPU and wireless communication modules are powered down, peripheral clocks are disabled, and all GPIOs are high-impedance | 180      |
|            | CPU, wireless communication modules and peripherals are powered down, and all GPIOs are high-impedance |          | 35       |
| Deep-sleep | RTC timer and LP memory are powered on                                                      | 7        |
| Power off  | CHIP_PU is set to low level, the chip is powered off                                        | 1        |

---

**Subtitle: Memory Specifications**

The data below is sourced from the memory vendor datasheet. These values are guaranteed through design and/or characterization but are not fully tested in production. Devices are shipped with the memory erased.

---

**Table 5-12. Flash Specifications**

| Parameter       | Description                           | Min    | Typ   | Max     | Unit |
|-----------------|---------------------------------------|--------|-------|---------|------|
| VCC             | Power supply voltage (1.8 V)         | 1.65   | 1.80  | 2.00    | V    |
|                 | Power supply voltage (3.3 V)         | 2.7    | 3.3   | 3.6     | V    |
| F_C             | Maximum clock frequency               | —      | —     | MHz     |      |
|                 | Program/erase cycles                 | 100,000|       | cycles  |      |
| TRet            | Data retention time                   | 20     |       | years   |      |
| Tpp             | Page program time                    | —      | 0.8   | 5      | ms   |
| Tse             | Sector erase time (4 KB)              | 70     |       | 500    | ms   |
| TB1             | Block erase time (32 KB)              | 0.2    |       | s       |      |
| TB2             | Block erase time (64 KB)              | —      | 0.3   | 3      | s    |
| Tce1            | Chip erase time (16 MB)               | 7      |       | 20     | s    |
|                 | Chip erase time (32 MB)               |        | 20    | 60     | s    |
| Tce2            | Chip erase time (64 MB)               | —      | 25   | 100    | s    |
|                 | Chip erase time (128 MB)              |       | 60    | 200    | s    |
|                 | Chip erase time (256 MB)              |       | 70   | 300    | s    |

---

**Subtitle: Reliability**

---

**Table 5-13. Reliability Qualifications**

| Test Item      | Test Conditions                                                                                   | Test Standard        |
|----------------|--------------------------------------------------------------------------------------------------|----------------------|
| HTOL (High Temperature Operating Life)         | 125 °C, 1000 hours                                                                               | JESD22-A108          |
| ESD (Electro-Static Discharge Sensitivity)      | HBM (Human Body Mode) ± 2000 V                                                                   | JS-001               |
|                 | CDM (Charge Device Mode) ^2 ± 1000 V                                                            | JS-002               |
| Latch up       | Current trigger ± 200 mA                                                                         |                     |
|                 | Voltage trigger 1.5 x VDD_max                                                                   | JESD78               |

---

**Footer:**

Espressif Systems

ESP32-C6 Series Datasheet v1.4
Submit Documentation Feedback