**Title: Electrical Characteristics**

---

### Section Title

6.4 Current Consumption Characteristics

#### Subsection:

6.4.1 Current Consumption in Active Mode

With the use of advanced power-management technologies, the module can switch between different power modes. For details on different power modes, please refer to Section Power Management Unit in ESP32-S3 Series Datasheet.

The current consumption measurements are taken with a 3.3 V supply at 25 °C ambient temperature.
- TX current consumption is rated at a 100% duty cycle
- RX current consumption is rated when the peripherals are disabled and the CPU idle

#### Table: Current Consumption for Wi-Fi (2.4 GHz) in Active Mode

| Work Mode | RF Condition           | Description                   | Peak (mA) |
|-----------|------------------------|-------------------------------|-----------|
|           | 802.11b, 1 Mbps, @20.5 dBm |                           | 355       |
| TX        |                        |                               |           |
| Active (RF working) | 802.11g, 54 Mbps, @18 dBm   |                           | 297       |
| RX        | 802.11n, HT20, MCS 7, @17.5 dBm |                   | 286       |
|           |                        |                               |           |
|           | 802.11n, HT40, MCS 7, @17 dBm |               | 285       |
| RX        | 802.11b/g/n, HT20      |                               | 95        |
|           |                        |                               |           |
|           | 802.11n, HT40         |                               | 97        |

#### Table: Current Consumption for Bluetooth LE in Active Mode

| Work Mode | RF Condition           | Description                   | Peak (mA) |
|-----------|------------------------|-------------------------------|-----------|
| TX        | Bluetooth LE @ 20.0 dBm   |                           | 340       |
| Active (RF working) | Bluetooth LE @ 9.0 dBm    |                           | 204       |
|           |                        |                               |           |
|           | Bluetooth LE @ 0 dBm     |                           | 189       |
| RX        | Bluetooth LE @ -15.0 dBm   |                           | 118       |
|           | Bluetooth LE            |                               | 93        |

#### Note:
The content below is excerpted from Section Power Consumption in Other Modes in ESP32-S3 Series Datasheet.

---

### Subsection:

6.4.2 Current Consumption in Other Modes

Please note that if the chip embedded has in-package PSRAM, the current consumption of the module might be higher compared to the measurements below.
- TX
- RX (not detailed)

---

**Footer:**

Espressif Systems  
30 ESP32-S3-MINI-1 & MINI-1U Datasheet v1.6

Submit Documentation Feedback