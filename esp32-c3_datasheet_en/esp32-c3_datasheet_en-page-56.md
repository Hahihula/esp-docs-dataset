**Title: Electrical Characteristics**

---

### Section Title

#### Subtitle (5.5): ADC Characteristics

##### Table Description:
- **Table Name:** Table 5-5. ADC Characteristics

| Symbol | Parameter | Min | Max | Unit |
|--------|-----------|-----|-----|------|
| DNL (Differential nonlinearity) <sup>1</sup> | ADC connected to an external 100 nF capacitor; DC signal input; Ambient temperature at 25 °C; Wi-Fi off | -7 | 7 | LSB |
| INL (Integral nonlinearity) | -12 | 12 | LSB |
| Sampling rate | — | — | 100 kSPS <sup>2</sup> |

**Footnotes:**
1. To get better DNL results, you can sample multiple times and apply a filter, or calculate the average value.
2. kSPS means kilo samples-per-second.

The calibrated ADC results after hardware calibration and software calibration are shown in Table 5-6. For higher accuracy, you may implement your own calibration methods.

---

##### Subtitle (Table Name): Table Description

| Parameter | Description | Min | Max | Unit |
|-----------|-------------|-----|-----|------|
| ATTEN10, effective measurement range of 0 ~ 750 | — | -10 | 10 | mV |
| ATTEN11, effective measurement range of 0 ~ 1050 | — | -10 | 10 | mV |
| Total error | <sup>3</sup> | — | — | mV |
| ATTEN12, effective measurement range of 0 ~ 1300 | — | -10 | 10 | mV |
| ATTEN13, effective measurement range of 0 ~ 2500 | <sup>4</sup> | -35 | 35 | mV |

**Footnotes:**
<sup>3</sup>. The current consumption measurements are taken with a 3.3 V supply at ambient temperature.
<sup>4</sup>. All transmitters' measurements are based on a 100% duty cycle.

---

#### Subtitle (5.6): Current Consumption

##### Section Title:

**Subsection: RF Current Consumption in Active Mode**

The current consumption measurements are taken with a 3.3 V supply at ambient temperature of the RF port. All transmitters' measurements are based on a 100% duty cycle.

---

##### Table Description:
- **Table Name:** Table 5-7. Wi-Fi Current Consumption Depending on RF Modes

| Work Mode | Description | Peak (mA) |
|-----------|-------------|-----------|
| TX        | 802.11b, 1 Mbps, @21 dBm | 335 |
|           | 802.11g, 54 Mbps, @19 dBm | 285 |
|           | 802.11n, HT20, MCS7, @18.5 dBm | 276 |
| Active (RF working) | 802.11n, HT40, MCS7, @18.5 dBm | 278 |
| RX        | 802.11b/g/n, HT20 | 84 |
|           | 802.11n, HT40 | 87 |

---

**Footer:**
Espressif Systems  
Page Number: 56  
ESP32-C3 Series Datasheet v2.2

Submit Documentation Feedback