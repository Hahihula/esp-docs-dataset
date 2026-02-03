**Title:**
6 Electrical Characteristics

**Subtitle and Notes:**
- VILnRST Chip reset voltage –0.3 ——– 0.25 × VDD1 V
  - Note (1): VDD is the I/O voltage for pins of a particular power domain.
  - Note (2): VOH and VOL are measured using high-impedance load.

**Section Title:**
6.4 Current Consumption Characteristics

**Subsection Titles with Content:**

*6.4.1 Current Consumption in Active Mode*
The current consumption measurements are taken with a 3.3 V supply at 25 °C ambient temperature.
- TX current consumption is rated at a 100% duty cycle.

- RX current consumption is rated when the peripherals are disabled and the CPU idle.

**Table Titles:**
- Table 15: Current Consumption for Wi-Fi (2.4 GHz) in Active Mode

| Work Mode | RF Condition       | Description                   | Peak (mA) |
|-----------|--------------------|-------------------------------|-----------|
|           |                    |                               |           |
| TX        | 802.11b, 1 Mbps, DSSS @20.5 dBm |                         | 370       |
|          | 802.11g, 54 Mbps, OFDM @18.5 dBm |                        | 308       |
|          | 802.11n, HT20, MCS7 @17.5 dBm   |                           | 289       |
| Active (RF working) | 802.11n, HT40, MCS7 @17 dBm    |                          | 269       |
|          | 802.11ax, MCS9 @14.5 dBm        |                           | 240       |
| RX       | 802.11b/g/n, HT20     |                               | 84        |
|          | 802.11n, HT40         |                               | 87        |
|          | 802.11ax, HE20        |                               | 84        |

**Table Title:**
- Table 16: Current Consumption for Bluetooth LE in Active Mode

| Work Mode | RF Condition       | Description                   | Peak (mA) |
|-----------|--------------------|-------------------------------|-----------|
|           |                    |                               |           |
| TX        | Bluetooth LE @ 18dBm   |                             | 310       |
|          | Bluetooth LE @ 9dBm    |                            | 170       |
| Active (RF working) | Bluetooth LE @ OdBm     |                           | 135       |
|          | Bluetooth LE @ –15dBm  |                          | 95        |
| RX       | Bluetooth LE         |                               | 80        |

**Footer:**
Espressif Systems
26 ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6

**Link:**
Submit Documentation Feedback