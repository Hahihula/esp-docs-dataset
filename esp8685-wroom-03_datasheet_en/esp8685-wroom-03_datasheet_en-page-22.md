**Title: Electrical Characteristics**

---

### Section Header

6.4 Current Consumption Characteristics

#### Subsection Title

6.4.1 RF Current Consumption in Active Mode

The current consumption measurements are taken with a 3.3 V supply at 25 °C ambient temperature.

TX current consumption is rated at a 100% duty cycle.
RX current consumption is rated when the peripherals are disabled and the CPU idle.

**Table Title**

Table 6-4: Current Consumption Depending on RF Modes

| Work mode | RF Condition | Description                                   | Peak (mA) |
|-----------|--------------|-----------------------------------------------|-----------|
|           |              | 802.11b, 1 Mbps, @20 dBm                     | 340       |
| TX        |              |                                                |           |
| Active (RF working) |     | 802.11g, 54 Mbps, @17.5 dBm                  | 278       |
|            |             | 802.11n, HT20, MCS7, @17 dBm                 | 267       |
|            |             | 802.11n, HT40, MCS7, @16.5 dBm               | 201       |
| RX        |              | 802.11b/g/n, HT20                             | 84        |
|           |              | 802.11n, HT40                                | 86        |

**Note**

The content below is excerpted from Section Power Consumption in Other Modes in ESP8685 Series Datasheet.

---

#### Subsection Title

6.4.2 Current Consumption in Other Modes

**Table Title**

Table 6-5: Current Consumption in Modem-sleep Mode

| Mode          | CPU Frequency (MHz) | Description                   | All Peripherals Clocks Disabled (mA) | All Peripherals Clocks Enabled (mA) |
|---------------|----------------------|-------------------------------|---------------------------------------|-------------------------------------|
|                |                      |                               |                                       |                                      |
| 160           | Modem-sleep         | CPU is running                 | 23                                    | 28                                  |
|               |                      | CPU is idle                   | 16                                    | 21                                  |
| 80            |                      | CPU is running                 | 17                                    | 22                                  |
|               |                      | CPU is idle                   | 13                                    | 18                                  |

**Footnotes**

1. In practice, the current consumption might be different depending on which peripherals are enabled.
2. In Modem-sleep mode, Wi-Fi is clock gated.
3. In Modem-sleep mode, the consumption might be higher when accessing flash. For a flash rated at 80 Mbit/s, in SPI 2-line mode the consumption is 10 mA.

---

**Footer**

Espressif Systems  
Page number: 22  
Document version: ESP8685-WROOM-03 Datasheet v1.5

Submit Documentation Feedback