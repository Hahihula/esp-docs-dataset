**Title: Electrical Characteristics**

---

### Table 6-6. Current Consumption in Low-Power Modes

| Mode          | Description                                                                                   | Typ (µA) |
|---------------|------------------------------------------------------------------------------------------------|----------|
| Light-sleep   | VDD_SPI and Wi-Fi are powered down, and all GPIOs are high-impedance                           | 130      |
| Deep-sleep    | RTC timer + RTC memory                                                                         | 5        |
| Power off     | CHIP_EN is set to low level, the chip is powered off                                          | 1        |

---

**Subtitle: Memory Specifications**

The data below is sourced from the memory vendor datasheet. These values are guaranteed through design and/or characterization but are not fully tested in production. Devices are shipped with the memory erased.

### Table 6-7. Flash Specifications

| Parameter     | Description                                    | Min   | Typ    | Max   | Unit |
|---------------|-----------------------------------------------|-------|--------|-------|------|
| VCC           | Power supply voltage (1.8 V)                  | 1.65  | 1.80   | 2.00  | V    |
|               | Power supply voltage (3.3 V)                  | 2.7   | 3.3    | 3.6   | V    |
| Fc            | Maximum clock frequency                        | —     | 80     | —     | MHz  |
| Program/erase cycles | Program/erase cycles                          | 100,000 |        |       |      |
| TRet          | Data retention time                            | 20    |        | years |      |
| TPP           | Page program time                              | 0.8   |        | 5     | ms   |
| TSE           | Sector erase time (4 KB)                       | —     | 70    | 500  | ms   |
| TE1           | Block erase time (32 KB)                       |       | 0.2   | 2     | s    |
| TE2           | Block erase time (64 KB)                       |       | 0.3   | 3     | s    |
| TCE1          | Chip erase time (16 Mb)                        |       | 7     | 20    | s    |
| TCE2          | Chip erase time (32 Mb)                        |       | 20    | 60    | s    |
| TCE3          | Chip erase time (64 Mb)                        |       | 25    | 100   | s    |
| TCE4          | Chip erase time (128 Mb)                       |       | 60    | 200   | s    |
| TCE5          | Chip erase time (256 Mb)                       |       | 70    | 300   | s    |

---

**Footer:**

Espressif Systems  
Page number and document version information at the bottom.