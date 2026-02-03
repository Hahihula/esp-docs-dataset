**Title: Electrical Characteristics**

---

### Table 6-9. Current Consumption in Low-Power Modes

| Mode       | Description                                                                                   | Typ (mA) |
|------------|----------------------------------------------------------------------------------------------|----------|
| Light-sleep| CPU and wireless communication modules are powered down, peripheral clocks are disabled, and all GPIOs are high-impedance | 0.25     |
|            | CPU, wireless communication modules and peripherals are powered down, and all GPIOs are high-impedance |          |
| Deep-sleep | RTC timer and LP memory are powered on                                                      | 0.012    |
| Power off  | CHIP_PU is set to low level, the chip is powered off                                        | 0.002    |

---

**Subtitle: Memory Specifications**

The data below is sourced from the memory vendor datasheet. These values are guaranteed through design and/or characterization but are not fully tested in production. Devices are shipped with the memory erased.

---

### Table 6-10. Flash Specifications

| Parameter | Description                   | Min   | Typ    | Max     | Unit |
|-----------|-------------------------------|-------|--------|---------|------|
| VCC       | Power supply voltage (1.8 V) | 1.65  | 1.80   | 2.00    | V    |
|           |                               | 3.3 V |        |         |      |
| FC        | Maximum clock frequency     | -     | —      | MHz     |      |
|           |                              |       |        |         |      |
| TRet      | Data retention time          | 20    | years | —       |      |
| TPP       | Program page time            | –     | 0.8   | 5      | ms   |
| TSE       | Sector erase time (4 KB)     | -     | 70    | 500    | ms   |
| TE1       | Block erase time (32 KB)     | -     | –     | s       |      |
| TE2       | Block erase time (64 KB)     | -     | —     | s       |      |
|           |                             | 7     |        |         |      |
| TCE       | Chip erase time (16 MB)      |    –  | 20    | 60     | s    |
|           |                             | 32 M |        |         |      |
|           |                             | 64 M |        |         |      |
|           |                             | 128 M|       | 200    | s    |
|           |                             | 256 M|       | 70     | s    |

---

### Table 6-11. PSRAM Specifications

| Parameter | Description                   | Min   | Typ    | Max     | Unit |
|-----------|-------------------------------|-------|--------|---------|------|
| VCC       | Power supply voltage (1.8 V) | 1.62  | 1.80   | 1.98    | V    |
|           |                               | 3.3 V |        |         |      |
| FC        | Maximum clock frequency     | –     | —      | MHz     |      |

---

**Footer:**

Espressif Systems  
ESP32-C5-MINI-1 Datasheet v1.0

Submit Documentation Feedback