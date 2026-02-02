**Title: Electrical Characteristics**

---

### Section Title

6.4 Current Consumption Characteristics

#### Subsection:

6.4.1 Current Consumption in Active Mode

The current consumption measurements are taken with a 3.3 V supply at 25 °C ambient temperature.

- **TX (Transmitter) current consumption** is rated at a *100% duty cycle*.
- **RX (Receiver) current consumption** is rated when the peripherals are disabled and the CPU idle.

---

#### Table: Current Consumption for Wi-Fi (2.4 GHz) in Active Mode

| Work Mode | RF Condition | Description                                   | Peak (mA) |
|-----------|--------------|-----------------------------------------------|-----------|
|           | 802.11b, 1 Mbps, DSSS @ 20.5 dBm            |                                               | 382      |
| TX        | 802.11g, 54 Mbps, OFDM @ 19.0 dBm            |                                               | 316      |
|           | 802.11n, HT20, MCS7 @ 18.0 dBm              |                                               | 295      |
| Active (RF working) | 802.11n, HT40, MCS7 @ 17.5 dBm |                                               | 280      |
|           | 802.11ax, MCS9 @ 15.5 dBm                   |                                               | 251      |
|           | 802.11b/g/n, HT20                          |                                               | 78       |
| RX        | 802.11n, HT40                               |                                               | 82       |
|           | 802.11ax, HE20                             |                                               | 78       |

---

#### Table: Current Consumption for Bluetooth LE in Active Mode

| Work Mode | RF Condition | Description                                   | Peak (mA) |
|-----------|--------------|-----------------------------------------------|-----------|
|           | Bluetooth LE @ 19.0 dBm                     |                                               | 309      |
| TX        | Bluetooth LE @ 9.0 dBm                       |                                               | 190      |
| Active (RF working) | Bluetooth LE @ -16.0 dBm |                                               | 130      |
|           | Bluetooth LE                                   |                                               | 93       |
| RX        | Bluetooth LE                                    |                                               | 73       |

---

#### Table: Current Consumption for 802.15.4 in Active Mode

| Work Mode | RF Condition | Description                                   | Peak (mA) |
|-----------|--------------|-----------------------------------------------|-----------|
|           | 802.15.4 @ 19.0 dBm                          |                                               | 302      |
| TX        | 802.15.4 @ 12.0 dBm                           |                                               | 185      |
| Active (RF working) | 802.15.4 @ -6.0 dBm |                                               | 97       |
|           | 802.15.4 @ 0 dBm                              |                                               | 117      |
| RX        | 802.15.4 @ -16.0 dBm                          |                                               | 91       |
|           | 802.15.4                                   |                                               | 73       |

---

**Footer:**

Espressif Systems  
ESP32-C6-G-WROOM-1 & WROOM-1U Datasheet v1.4

Submit Documentation Feedback