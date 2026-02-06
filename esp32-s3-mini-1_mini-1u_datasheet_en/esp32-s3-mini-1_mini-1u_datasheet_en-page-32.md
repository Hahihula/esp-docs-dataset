**Title:**
6 Electrical Characteristics

**Body Text:**

- **Power off:** EN is set to low level. The chip is shut down.

1 In Light-sleep mode, all related SPI pins are pulled up. For chips embedded with PSRAM, please add corresponding PSRAM consumption values, e.g., 140 µA for 8 MB Octal PSRAM (3.3 V), 200 µA for 8 MB Octal PSRAM (1.8 V) and 40 µA for 2 MB Quad PSRAM (3.3 V).

**Subtitle:**
6.5 Memory Specifications

The data below is sourced from the memory vendor datasheet. These values are guaranteed through design and/or characterization but are not fully tested in production. Devices are shipped with the memory erased.

**Table - Title:** Table 6-8. Flash Specifications
| Parameter | Description                | Min   | Typ    | Max     | Unit |
|-----------|-----------------------------|-------|--------|---------|------|
| VCC       | Power supply voltage (1.8 V) | 1.62  | 1.80   | 2.00    | V    |
|           | Power supply voltage (3.3 V) | 2.7   | 3.3    | 3.6     | V    |
| FC        | Maximum clock frequency     | —     | 80     | —       | MHz  |
| —         | Program/erase cycles       | 100,000 |      | —       | cycles|
| TRet      | Data retention time         | 20    | —      | years   |      |
| TPP       | Page program time          | 0.8   |        | 5       | ms   |
| TSE       | Sector erase time (4 KB)    | 70    |        | 500     | ms   |
| TB1E      | Block erase time (32 KB)    | —     | 0.2    | 2       | s    |
| TB2E      | Block erase time (64 KB)    | —     | 0.3    | 3       | s    |
| TCE       | Chip erase time (16 MB)     |        | 7      | 20      | s    |
|           |                             | 20    |        | 60      | s    |
|           |                             | 25    |        | 100     | s    |
|           |                             | 60    |        | 200     | s    |
|           |                             | 70    |        | 300     | s    |

**Table - Title:** Table 6-9. PSRAM Specifications
| Parameter | Description                | Min   | Typ    | Max     | Unit |
|-----------|-----------------------------|-------|--------|---------|------|
| VCC       | Power supply voltage (1.8 V) | 1.62  | 1.80   | 1.98    | V    |
|           | Power supply voltage (3.3 V) | 2.7   | 3.3    | 3.6     | V    |
| FC        | Maximum clock frequency     | —     | 80     | —       | MHz  |

**Footer:**
Espressif Systems
Page number: 32

Link text:
Submit Documentation Feedback