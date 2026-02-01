**Title: Electrical Characteristics**

---

### Table 5-8. Current Consumption for Bluetooth LE in Active Mode

| Work Mode | RF Condition       | Description                                      | Peak (mA) |
|-----------|--------------------|--------------------------------------------------|------------|
|           | TX                 | Bluetooth LE @ 21.0 dBm                         | 335        |
|           |                    | Bluetooth LE @ 9.0 dBm                          | 193        |
| Active (RF working) |                | Bluetooth LE @ 0 dBm                            | 176        |
|           | RX                 | Bluetooth LE @ -15.0 dBm                        | 116        |
|           |                    | Bluetooth LE                                    | 93         |

---

### Section: Current Consumption in Other Modes

The measurements below are applicable to ESP32-S3 and ESP32-S3FH8. Since ESP32-S3R2, ESP32-S3RH2, ESP32-S3R8, ESP32-S3R8V, ESP32-S3R16V, and ESP32-S3FN4R2 are embedded with PSRAM, their current consumption might be higher.

---

### Table 5-9. Current Consumption in Modem-sleep Mode

| Work mode | Frequency (MHz) | Description                                                                                   | Typ^1 (mA) | Typ^2 (mA) |
|-----------|-----------------|------------------------------------------------------------------------------------------------|------------|------------|
|           |                 | Description                                                                                   |            |            |
| 40        | WAITI           | Dual core running 32-bit data access instructions, the other core in idle state                  | 16.2       | 21.8       |
| 80        |                 | Single core running 32-bit data access instructions, the other core in idle state                | 19.9       | 25.4       |
|           | WAITI           | Dual core running 128-bit data access instructions                                               | 23.0       | 28.8       |
|           |                 | Single core running 32-bit data access instructions, the other core in idle state                | 27.6       | 42.3       |
|           | WAITI           | Dual core running 128-bit data access instructions                                               | 29.0       | 56.3       |
| Modem-sleep^3 |         | Single core running 32-bit data access instructions, the other core in idle state                | 47.3       | 54.6       |
|           |                 | Dual core running 128-bit data access instructions                                               | 50.9       | 64.1       |
| 160       | WAITI           | Single core running 32-bit data access instructions, the other core in idle state                | 72.4       | 87.9       |

---

**Footer:**
Espressif Systems
Page number: 67

Submit Documentation Feedback ESP32-S3 Series Datasheet v2.1