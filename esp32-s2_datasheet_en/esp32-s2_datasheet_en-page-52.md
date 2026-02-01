Title: Electrical Characteristics

Body Text:
1 In Light-sleep mode, with all related SPI pins pulled up, the current consumption of the embedded PSRAM is 140 µA. Chip variants with in-package PSRAM include ESP32-S2FN4R2 and ESP32-S2R2.
2 During Deep-sleep, when the ULP co-processor is powered on, peripherals such as GPIO and I2C are able to operate.

The "ULP sensor-monitored pattern" refers to the mode where the ULP coprocessor or the sensor works periodically. When touch sensors work with a duty cycle of 1%, the typical current consumption is 22 µA.

Subtitle: Memory Specifications

Body Text:
The data below is sourced from the memory vendor datasheet. These values are guaranteed through design and/or characterization but are not fully tested in production. Devices are shipped with the memory erased.

Table Title: Table 5-10. Flash Specifications
| Parameter | Description | Min | Typ | Max | Unit |
|-----------|-------------|-----|-----|-----|------|
| VCC       | Power supply voltage (1.8 V) | 1.65 | - | 2.00 | V   |
|           | Power supply voltage (3.3 V) | 2.7 | - | 3.6 | V   |
| FC        | Maximum clock frequency | — | 80 | – | MHz |
| —        | Program/erase cycles | 100,000 |— |– |cycles|
| TRet     | Data retention time | 20 | - | years | |
| TPP      | Page program time | 0.8 |- |5 |ms |
| SSE      | Sector erase time (4 KB) | — |70 | – |500 ms |
| BE1      | Block erase time (32 KB) |— |– |0.2 |s |
| BE2      | Block erase time (64 KB) | 0.3 | - | 3 | s |
| Chip erase time (16 Mb) | — |7 | – |20 | s |
| Chip erase time (32 Mb) |— |– |20 | – |60 |s|
| CE       | Chip erase time (64 Mb) | - | 25 |—— |100 |s|
|         | Chip erase time (128 Mb) | — |- |60 |200 s |
|         | Chip erase time (256 Mb) |— |– |70 |300 s |

Subtitle: Reliability

Table Title: Table 5-11. Reliability Qualifications
| Test Item       | Test Conditions | Test Standard |
|-----------------|-----------------|---------------|
| HTOL (High Temperature Operating Life) | 125 °C, 1000 hours | JESD22-A108 |
| ESD (Electro-Static Discharge Sensitivity) | HBM (Human Body Mode) ± 2000 V; CDM (Charge Device Mode) ± 1000 V | JS-001, JS-002 |
| Latch up       | Current trigger ± 200 mA Voltage trigger 1.5 × VDDmax | JESD78 |

Footer:
Espressif Systems
Page number: 52

Link Texts:
Submit Documentation Feedback ESP32-S2 Series Datasheet v1.8