**Title: Electrical Characteristics**

---

### Table Summary

- **Table Title:** Current Consumption in Low-Power Modes (Table 5-10)
- **Columns:** Work mode, Description, Type (\(\mu\)A)

| Work mode | Description                                                                                   | Typ (\(\mu\)A) |
|-----------|------------------------------------------------------------------------------------------------|---------------|
| Light-sleep^1 | VDD_SPI and Wi-Fi are powered down, and all GPIOs are high-impedance                         | 240           |
| Deep-sleep | RTC memory and RTC peripherals are powered up. RTC peripherals are powered down.             | 8             |
| Power off  | CHIP PU is set to low level. The chip is shut down.                                        | 1             |

Footnotes:
- ^1 In Light-sleep mode, all related SPI pins are pulled up.
- For chips embedded with PSRAM, please add corresponding PSRAM consumption values.

---

### Section: Memory Specifications

**Subtitle:** Flash Specifications (Table 5-11)

| Parameter       | Description                                    | Min   | Max   | Typ Unit |
|-----------------|-----------------------------------------------|-------|-------|----------|
| VCC             | Power supply voltage (1.8 V)                  | 1.65  | 2.00  | V        |
|                 | Power supply voltage (3.3 V)                  | 2.7   | 3.6   | V        |
| \(F_C\)         | Maximum clock frequency                        | —     | —     | MHz      |
| Program/erase cycles | —                                               | 100,000— | cycles    |
| \(T_{RET}\)     | Data retention time                            | 20    | —     | years   |
| \(T_{PP}\)      | Page program time                              | —     | 5 ms  |         |
| \(T_{SE}\)      | Sector erase time (4 KB)                       | 70    | 500   | ms       |
| \(T_{BE1}\)     | Block erase time (32 KB)                       | 0.2   | 2 s    |         |
| \(T_{BE2}\)     | Block erase time (64 KB)                       | —     | 3 s    |         |
| \(T_{CE}\)      | Chip erase time (16 Mb)                        | —     | 7     | s        |
|                 | Chip erase time (32 Mb)                        | —     | 20    | s        |
|                 | Chip erase time (64 Mb)                        | —     | 60    | s        |

---

**Footer:** Espressif Systems, ESP32-S3 Series Datasheet v2.1

---

### Additional Notes
- Current consumption when all peripheral clocks are disabled.
- In practice, the current consumption might be different depending on which peripherals are enabled.

In Modem-sleep mode:
- Wi-Fi is clock gated; and in SPI 2-line mode with a flash rated at 80 Mbit/s, the current consumption can reach up to approximately 10 mA.