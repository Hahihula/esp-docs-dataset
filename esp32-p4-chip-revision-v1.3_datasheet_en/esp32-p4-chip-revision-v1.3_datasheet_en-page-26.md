**Title:**
2 Pins

**Subtitle:**
2.4 Dedicated Interface Pins

**Body Text:**
Some pins are dedicated to a few important peripherals, such as MIPI DSI and MIPI CSI.

**Table 1 (Table 2-8): Peripheral-Dedicated Signals**

| Pin Function | Signal       | Description                                    |
|--------------|-------------|------------------------------------------------|
| FLASH_CS     | Chip select  |                                               |
| FLASH_Q      | Data output  |                                               |
| FLASH_WP     | Write protect|                                               |
| FLASH_HOLD   | Hold         | Flash connection                              |
| FLASH_CK     | Clock        |                                               |
| FLASH_D      | Data in      |                                               |
| MIPI DSI PHY 4.02 kΩ EXTERNAL | External resistor 4.02 kΩ |                   |
| RESISTOR     |             |                                               |
| MIPI DSI PHY DATAP... | Data positive channel 0/1 | MIPI DSI connection                          |
|               |            |                                               |
|               |            |                                               |
| MIPI CSI PHY CLKN | Clock negative channel |                                               |
| MIPI CSI PHY CLKP | Clock positive channel |                                               |
| MIPI CSI PHY 4.02 kΩ EXTERNAL | External resistor 4.02 kΩ |                                               |
| RESISTOR     |             |                                               |
| MIPI CSI PHY DATAP... | Data positive channel 0/1 | MIPI CSI connection                          |
|               |            |                                               |
| MIPI CSI PHY DATAN... | Data negative channel 0/1 |                                               |
| MIPI CSI PHY CLKN | Clock negative channel |                                               |
| MIPI CSI PHY CLKP | Clock positive channel |                                               |
| USB2 OTG PHY DM | USB D-      | USB 2.0 high-speed OTG connection              |
| USB2 OTG PHY DP | USB D+      |                                               |

**Table 2 (Table 2-9): Dedicated Interface Pins**

| Pin No | Dedicated Interface Pin | Function       | Type    |
|--------|-------------------------|----------------|---------|
|        |                         |                |         |
| 27     | FLASH_CS                | FLASH_CS       | I/O/T   |
| 28     | FLASH_Q                 | FLASH_Q        | I/O/T   |
| 29     | FLASH_WP                | FLASH_WP       | I/O/T   |
| 31     | FLASH_HOLD              | FLASH_HOLD     | I/O/T   |
| 32     | FLASH_CK                | FLASH_CK       | O       |
| 33     | FLASH_D                 | FLASH_D        | I/O/T   |
| 34     | DSI_REXT                | MIPI DSI PHY 4.02 kΩ EXTERNAL RESISTOR | I/O/T |
| 35     | DSI_DATAP1              | MIPI DSI PHY DATAP1 | I/O/T |
| 36     | DSI_DATA1               | MIPI DSI PHY DATAN1 | I/O/T |
| 37     | DSI_CLKN                | MIPI DSI PHY CLKN | I/O/T |
| 38     | DSI_CLKP                | MIPI DSI PHY CLKP | I/O/T |
| 39     | DSI_DATAPO              | MIPI DSI PHY DATAPO | I/O/T |

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-P4 Series Datasheet v0.6