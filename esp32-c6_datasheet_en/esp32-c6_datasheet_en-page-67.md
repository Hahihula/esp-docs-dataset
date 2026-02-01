**Title: Electrical Characteristics**

---

### Table 5-7 – cont’d from previous page

| Work Mode | RF Condition       | Description                          | Peak (mA) |
|-----------|--------------------|--------------------------------------|------------|
|           |                    |                                      |            |
| RX        | 802.11b/g/n, HT20   |                                      | 78         |
|          | 802.11n, HT40      |                                      | 82         |
|          | 802.11ax, HE20     |                                      | 78         |

---

### Table 5-8. Current Consumption for Bluetooth LE in Active Mode

| Work Mode       | RF Condition        | Description                          | Peak (mA) |
|-----------------|--------------------|--------------------------------------|------------|
|                 |                    |                                      |            |
| TX              | Bluetooth LE @ 20.0 dBm |                               | 315        |
| Active (RF working)| Bluetooth LE @ 9.0 dBm   |                                   | 190        |
|                  | Bluetooth LE @ 0 dBm    |                                    | 130        |
|                  | Bluetooth LE @ -15.0 dBm |                                  | 94         |
| RX              | Bluetooth LE          |                                      | 71         |

---

### Table 5-9. Current Consumption for 802.15.4 in Active Mode

| Work Mode       | RF Condition        | Description                          | Peak (mA) |
|-----------------|--------------------|--------------------------------------|------------|
|                 |                    |                                      |            |
| TX              | 802.15.4 @ 20.0 dBm |                               | 305        |
| Active (RF working)| 802.15.4 @ -12.0 dBm   |                                   | 187        |
|                  | 802.15.4 @ 0 dBm     |                                    | 119        |
| RX              | 802.15.4 @ -15.0 dBm |                                  | 92         |
|                  | 802.15.4            |                                      | 74         |

---

### Section: Current Consumption in Other Modes

#### Subsection Title: Table 5-10. Current Consumption in Modem-sleep Mode

| Mode          | CPU Frequency (MHz) | Description                          | All Peripherals Typ (mA) |
|---------------|---------------------|--------------------------------------|--------------------------|
|               |                     |                                      |                          |
| Modem-sleep 2,3 |                   | CPU is running                      | 17                       |
|                |                    | CPU is idle                          | 80                       |

---

**Footnotes:**
1. In practice, the current consumption might be different depending on which peripherals are enabled.
2. In Modem-sleep mode, Wi-Fi is clock gated.
3. In Modem-sleep mode, the consumption might be higher when accessing flash.

---

**Footer:**  
Espressif Systems  
67  
ESP32-C6 Series Datasheet v1.4  
Submit Documentation Feedback