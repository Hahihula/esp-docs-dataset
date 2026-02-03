**Title: Electrical Characteristics**

---

### Table 6-6. Current Consumption for Bluetooth LE in Active Mode

| Work Mode | RF Condition | Description | Peak (mA) |
|-----------|--------------|-------------|-----------|
|           | TX           | Bluetooth LE @ 20.2dBm | 362       |
|           |              | Bluetooth LE @ 8.7dBm   | 206       |
| Active (RF working) |          | Bluetooth LE @ OdBm     | 168       |
|           | RX           | Bluetooth LE @ -15dBm    | 105       |
|           |              | Bluetooth LE         | 85        |

---

### Table 6-7. Current Consumption for 802.15.4 in Active Mode

| Work Mode | RF Condition | Description | Peak (mA) |
|-----------|--------------|-------------|-----------|
|           | TX           | 802.15.4 @ 20.2dBm   | 360       |
|           |              | 802.15.4 @ 8.2dBm    | 206       |
| Active (RF working) |          | 802.15.4 @ -1dBm     | 167       |
|           | RX           | 802.15.4 @ -15dBm    | 105       |
|           |              | 802.15.4            | 85        |

---

**Note:**
The content below is excerpted from Section Power Consumption in Other Modes in ESP32-C5 Series Datasheet.

---

### Subtitle: Current Consumption in Other Modes

#### Table 6-8. Current Consumption in Modem-sleep Mode

| Mode            | CPU Frequency (MHz) | Description                   | All Peripheral Typ (mA) | All Peripherals Clocks Enabled |
|-----------------|----------------------|-------------------------------|--------------------------|--------------------------------|
|                 |                      |                               |                         |                                 |
| WAITI           | 240                  | CPU while loop                | 18                       | 27                             |
| Run CoreMark    |                      |                               | 26                       | 35                             |
| WAITI           | 160                  | CPU while loop                | 15                       | 27                             |
| Run CoreMark    |                      |                               | 20                       | 32                             |
| WAITI           | 80                   | CPU while loop                | 12                       | 24                             |
| Run CoreMark    |                      |                               | 15                       | 26                             |
| WAITI           | 40                   | CPU while loop                | 8                        | 18                             |
| Run CoreMark    |                      |                               | 10                       | 19                             |
|                  |                      |                               | 12                       | 21                             |

---

**Footnotes:**
1. In practice, the current consumption might be different depending on which peripherals are enabled.
2. In Modem-sleep mode, Wi-Fi is clock gated.
3. In Modem-sleep mode, the consumption might be higher when accessing flash.

---

**Footer:**  
Espressif Systems  
ESP32-C5-MINI-1 Datasheet v1.0  
Submit Documentation Feedback