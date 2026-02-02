**Title: Electrical Characteristics**

---

### Table of Contents

- **6.4 Current Consumption Characteristics**
  - Subsection (6.4.1): Current Consumption in Active Mode

---

#### Section Header:
**Table 6-3 – cont’d from previous page**

| Parameter | Description                                   | Min   | Typ    | Max   | Unit |
|-----------|-----------------------------------------------|-------|--------|-------|------|
| \(R_{PD}\) | Internal weak pull-down resistor              | —     | 45     | —     | kΩ   |
| \(V_{IH_nRST}\) | Chip reset release voltage (CHIP_PU voltage is within the specified range) | -      | VDD\(^1\) + 0.3 | V    |
| \(V_{IL_nRST}\) | Chip reset voltage (CHIP_PU voltage is within the specified range) | —     | −0.3   | 0.25 × VDD\(^1\) | V    |

Footnotes:
1: VDD – voltage from a power pin of a respective power domain.
2: \(V_{OH}\) and \(V_{OL}\) are measured using high-impedance load.

---

#### Section Header (6.4):
**Current Consumption in Active Mode**

The current consumption measurements are taken with a 3.3 V supply at 25 °C ambient temperature.

TX current consumption is rated to a 100% duty cycle.
RX current consumption is rated when the peripherals are disabled and the CPU idle.

---

#### Table Header:
**Table 6-4: Current Consumption for Wi-Fi (2.4 GHz) in Active Mode**

| Work Mode | RF Condition           | Peak (mA) |
|-----------|------------------------|-----------|
|           |                        |           |
| **802.11b, 1 Mbps, DSSS @ 19dBm** | TX: 337 <br> RX: — |
|          |                        |           |
| **802.11g, 54 Mbps, OFDM @ 15.7dBm** | TX: 272 <br> RX: — |
|          |                        |           |
| **802.11n, HT20, MCS7 @ 15.9dBm** | TX: 272 <br> RX: — |
|          |                        |           |
| **802.11n, HT40, MCS7 @ 15dBm** | TX: 265 <br> RX: — |
|          |                        |           |
| **802.11ax, MCS9 @ 14dBm** | TX: 249 <br> RX: — |
|          |                        |           |
| **802.11ax/g/n, HT20** | TX: 94 <br> RX: 102 |
|          |                        |           |
| **802.11ax, HE20** | TX: — <br> RX: 94 |

---

#### Table Header:
**Table 6-5: Current Consumption for Wi-Fi (5 GHz) in Active Mode**

| Work Mode | RF Condition           | Peak (mA) |
|-----------|------------------------|-----------|
|           |                        |           |
| **802.11a, 6 Mbps, OFDM @ 17.5dBm** | TX: 397 <br> RX: — |
|          |                        |           |
| **802.11n, HT20, MCS7 @ 14.6dBm** | TX: 364 <br> RX: — |
|          |                        |           |
| **802.11n, HT40, MCS7 @ 14.4dBm** | TX: 361 <br> RX: — |
|          |                        |           |
| **802.11ac, VHT20, MCS7 @ 14.4dBm** | TX: 364 <br> RX: — |
|          |                        |           |
| **802.11ax, HE20, MCS7 @ 14.4dBm** | TX: 365 <br> RX: 121 |
|          |                        |           |
| **802.11ac, VHT20** | TX: — <br> RX: 120 |
|          |                        |           |
| **802.11ax, HE20** | TX: — <br> RX: 122 |

---

**Footer Information:**  
Espressif Systems  
Page Number: 33  
Document Title: ESP32-C5-WROOM-1 & WROOM-1U Datasheet v0.8  
Feedback Link Text: Submit Documentation Feedback  
Status Indicator (PRELIMINARY)