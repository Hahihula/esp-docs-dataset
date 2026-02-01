**Title: Electrical Characteristics**

---

### Table 5-6. Current Consumption for Wi-Fi (2.4 GHz) in Active Mode

| Work Mode | RF Condition       | Description                   | Peak (mA) |
|-----------|--------------------|-------------------------------|------------|
|           |                    |                               |            |
| TX        | 802.11b, 1 Mbps, DSSS @21 dBm |                                 | **360**   |
|          | 802.11g, 54 Mbps, OFDM @19 dBm |                                 | **310**   |
|          | 802.11n, HT20, MCS7 @18 dBm    |                                 | **285**   |
| Active (RF working) | 802.11n, HT40, MCS7 @17.5 dBm |                                 | **267**   |
|          | 802.11ax, MCS9 @15 dBm         |                                 | **240**   |
|          | 802.11b/g/n, HT20    |                                 | **88**     |
| RX        | 802.11n, HT40       |                                 | **90**     |
|          | 802.11ax, HE20       |                                 | **88**     |

---

### Table 5-7. Current Consumption for Bluetooth LE in Active Mode

| Work Mode | RF Condition       | Description                   | Peak (mA) |
|-----------|--------------------|-------------------------------|------------|
|           |                    |                               |            |
| TX        | Bluetooth LE @18 dBm    |                                 | **283**   |
|          | Bluetooth LE @9 dBm     |                                 | **160**   |
| Active (RF working) | Bluetooth LE @0 dBm      |                                 | **128**   |
|          | Bluetooth LE @-15 dBm    |                                 | **96**    |
| RX        | Bluetooth LE         |                                 | **81**    |

---

### 5.5.2 Current Consumption in Other Modes

#### Table 5-8. Current Consumption in Modem-sleep Mode

| Mode       | CPU Frequency (MHz) | Description                   | All Peripherals Typ (mA) | All Peripherals |
|------------|----------------------|-------------------------------|---------------------------|----------------|
| WAITI      |                      |                               |                          |                |
|            | 160                  | CPU while loop               | **11**                    | **18**         |
| Modem-sleep-2.3 |                      | Run CoreMark                 | **21**                    | **28**         |
| WAITI      |                      |                               |                          |                |
|            | 80                  | CPU while loop               | **10**                    | **16**         |
| Modem-sleep-3.9 |                      | Run CoreMark                 | **7**                     | **12**         |

---

Footnotes:
1 In practice, the current consumption might be different depending on which peripherals are enabled.
2 In Modem-sleep mode, Wi-Fi is clock gated.
3 In Modem-sleep mode, the consumption might be higher when accessing flash.

---

Espressif Systems  
57  
ESP32-C61 Series Datasheet v0.5