**Title: Electrical Characteristics**

---

### Table of Contents

- **6.4 Current Consumption Characteristics**
  - Subsection (6.4.1): *Current Consumption in Active Mode*

---

#### Section Header:
**Table 6-3 – cont’d from previous page**

| Parameter | Description                           | Min   | Typ    | Max   | Unit |
|-----------|---------------------------------------|-------|--------|-------|------|
| \(R_{PD}\) | Internal weak pull-down resistor      | —     | 45     | —     | kΩ   |
| \(V_{IH_nRST}\) | Chip reset release voltage (CHIP_PU voltage is within the specified range) | 0.75 × VDD^1 | —       | \(V\) |
| \(V_{IL_nRST}\) | Chip reset voltage (CHIP_PU voltage is within the specified range) | -0.3   | —      | 0.25 × VDD^1 | \(V\) |

Footnotes:
1: VDD – voltage from a power pin of a respective power domain.
2: \(V_{OH}\) and \(V_{OL}\) are measured using high-impedance load.

---

#### Subsection Header (6.4.1): *Current Consumption in Active Mode*

The current consumption measurements are taken with a 3.3 V supply at 25 °C ambient temperature.
- TX current consumption is rated to a 100% duty cycle
- RX current consumption is rated when the peripherals are disabled and the CPU idle.

---

#### Table Header:
**Table 6-4: Current Consumption for Wi-Fi (2.4 GHz) in Active Mode**

| Work Mode    | RF Condition           | Description                   | Peak (mA) |
|--------------|------------------------|-------------------------------|-----------|
|              |                        |                               |           |
| TX          |                         |                              | 323       |
|             |                         | 802.11b, 1 Mbps, DSSS @ 19.2dBm |            |
| Active (RF working) |                      |                              | 271       |
|              |                        | 802.11g, 54 Mbps, OFDM @ 16.4dBm |           |
| TX          |                         |                              | 271       |
|             |                         | 802.11n, HT20, MCS7 @ 16.5dBm |            |
|              |                        |                              | 271       |
| Active (RF working) |                      |                              | 263       |
| TX          |                         |                              | 249       |
|             |                         | 802.11n, HT40, MCS7 @ 15.6dBm |           |
|              |                        |                              | 94        |
| RX          |                         | 802.11ax, HT20                | 101       |
|             |                         | 802.11ax, HE20                | 94        |

---

#### Table Header:
**Table 6-5: Current Consumption for Wi-Fi (5 GHz) in Active Mode**

| Work Mode    | RF Condition           | Description                   | Peak (mA) |
|--------------|------------------------|-------------------------------|-----------|
|              |                        |                               |           |
| TX          |                         |                              | 395       |
|             |                         | 802.11a, 6 Mbps, OFDM @ 17.5dBm |            |
| Active (RF working) |                      |                              | 369       |
| TX          |                         | 802.11n, HT20, MCS7 @ 15dBm   | 364       |
|             |                         |                              | 354       |
|              |                        |                              | 368       |
| RX          |                         | 802.11ac, VHT20, MCS7 @ 15dBm |           |
|             |                         |                              | 367       |
| Active (RF working) |                      |                              | 121       |
| TX          |                         |                              | 128       |
|             |                         | 802.11n, HT40                 |           |
| RX          |                         | 802.11ac, VHT20               | 120       |
|              |                        |                              | 121       |

---

**Footer:**
Espressif Systems  
30  
Submit Documentation Feedback

ESP32-C5-MINI-1 Datasheet v1.0