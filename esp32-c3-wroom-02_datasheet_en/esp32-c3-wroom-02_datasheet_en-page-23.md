**Title: Electrical Characteristics**

---

### Section Header:
6.4 Current Consumption Characteristics

#### Subsection Title:
6.4.1 Current Consumption in Active Mode

#### Body Text:
The current consumption measurements are taken with a 3.3 V supply at 25 °C ambient temperature.

TX current consumption is rated at a 100% duty cycle.
RX current consumption is rated when the peripherals are disabled and the CPU idle.

**Table Title: Table 6-4. Current Consumption for Wi-Fi (2.4 GHz) in Active Mode**

| Work mode | Description                                      | Peak (mA) |
|-----------|---------------------------------------------------|-----------|
|           | 802.11b, 1 Mbps, @20.5 dBm                      | 345       |
| TX        |                                                   | 285       |
| Active (RF working) | 802.11g, 54 Mbps, @18 dBm                        | 280       |
|           | 802.11n, HT20, MCS7, @17.5 dBm                  | 280       |
| RX        | 802.11b/g/n, HT20                                 | 82        |
|           | 802.11g/40                                      | 84        |

**Note:**
The content below is excerpted from Section Power Consumption in Other Modes in ESP32-C3 Series Datasheet.

---

#### Subsection Title:
6.4.2 Current Consumption in Other Modes

#### Table Title: Table 6-5. Current Consumption in Modem-sleep Mode

| Mode         | CPU Frequency (MHz) | Description                   | All Peripherals Clocks Disabled (mA) | All Peripherals Clocks Enabled (mA) |
|--------------|----------------------|-------------------------------|---------------------------------------|-------------------------------------|
|              |                      |                               |                                       |                                     |
| 160         | Modem-sleep          | CPU is running                | 23                                    | 28                                   |
|             |                      | CPU is idle                   | 16                                    | 21                                   |
| 80          |                      | CPU is running                | 17                                    | 22                                   |
|             |                      | CPU is idle                   | 13                                    | 18                                   |

**Footnotes:**
1. In practice, the current consumption might be different depending on which peripherals are enabled.
2. In Modem-sleep mode, Wi-Fi is clock gated.
3. In Modem-sleep mode, the consumption might be higher when accessing flash. For a flash rated at 80 Mbit/s, in SPI 2-line mode the consumption is 10 mA.

---

**Footer:**
Espressif Systems
Page number and document reference information:
ESP32-C3-WROOM-02 & WROOM-02U Datasheet v1.6

Submit Documentation Feedback