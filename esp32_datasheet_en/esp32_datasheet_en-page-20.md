**Title:**
2 Pins

**Body Text:**

- When VDD_SDIO 1.8 V is used as the power supply for external flash/PSRAM, a 2 kΩ grounding resistor should be added to VDD_SDIO. For the circuit design, please refer to ESP32 Hardware Design Guidelines.
  
- When the three digital power supplies are used to drive peripherals, e.g., 3.3 V flash, they should comply with the peripherals' specifications.

**Subtitle:**
2.6 Pin Mapping Between Chip and Flash/PSRAM

**Table Description (Table 2-5):**

| ESP32-U4WDH | In-Package Flash (4 MB) |
|-------------|-------------------------|
| SD_DATA_1  | IO0/DI                  |
| GPIO17      | IO1/DO                  |
| SD_DATA_0  | IO2/WP#                 |
| SD_CMD      | IO3/HOLD#               |
| SD_CLK      | CLK                     |
| GPIO16     | CS#                     |
| GND         | VSS                     |
| VDD_SDIO    | VDD                     |

**Table Description (Table 2-5 - continued):**

| ESP32-D0WDRH2-V3 | In-Package PSRAM (2 MB) |
|------------------|-------------------------|
| SD_DATA_1       | SIO0/SI                 |
| SD_DATA_0       | SIO1/SO                 |
| SD_DATA_3       | SI02                    |
| SD_DATA_2       | SI03                    |
| SD_CLK          | SCLK                    |
| GPIO16^2       | CE#                     |
| GND            | VSS                     |
| VDD_SDIO        | VDD                     |

**Table Description (Table 2-6):**

| Chip Pin     | Off-Package Flash      |
|--------------|------------------------|
| SD_DATA_1/SPID | IO0/DI                 |
| SD_DATA_0/SPIQ | IO1/DO                 |
| SD_DATA_3/SPIWP | IO2/WP#                |
| SD_DATA_2/SPIHD | IO3/HOLD#              |
| SD_CLK       | CLK                    |
| SD_CMD       | CS#                    |
| GND         | VSS                    |
| VDD_SDIO    | VDD                    |

**Footer:**
Espressif Systems
ESP32 Series Datasheet v5.2

Submit Documentation Feedback