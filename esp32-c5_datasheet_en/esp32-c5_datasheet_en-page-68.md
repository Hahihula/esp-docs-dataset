Title: Electrical Characteristics

Subtitle: 5.5 ADC Characteristics

Body Text:
The measurements in this section are taken with an external 100 nF capacitor connected to the ADC, using DC signals as input, and at an ambient temperature of 25 °C with disabled Wi-Fi.

Table Title: Table 5-5. ADC Characteristics
- Symbol | Min | Max | Unit
- DNL (Differential nonlinearity)¹ | -5 | 5 | LSB
- INL (Integral nonlinearity) | -5 | 5 | LSB
- Sampling rate | — | 2000 | kSPS²

Footnotes:
1 To get better DNL results, you can sample multiple times and apply a filter, or calculate the average value.
2 kSPS means kilo samples-per-second.

Body Text: The calibrated ADC results after hardware calibration and software calibration are shown in Table 5-6. For higher accuracy, you may implement your own calibration methods.

Table Title: Table 5-6. ADC Calibration Results
- Parameter | Description | Min | Max | Unit
- ATTEN0, effective measurement range of 0 ~ 1000 | — | -10 | +10 | mV
- ATTEN1, effective measurement range of 0 ~ 1300 | — | -10 | +10 | mV
- Total error | — | — | –12 | +12 | mV
- ATTEN2, effective measurement range of 0 ~ 1900 | — | -15 | +15 | mV
- ATTEN3, effective measurement range of 0 ~ 3300 | — | -15 | +15 | mV

Title: 5.6 Current Consumption

Subtitle: RF Current Consumption in Active Mode

Body Text:
The current consumption measurements are taken with a 3.3 V supply at 25 °C ambient temperature.
TX current consumption is rated at a 100% duty cycle.

RX current consumption is rated when the peripherals are disabled and the CPU idle.

Table Title: Table 5-7. Current Consumption for Wi-Fi (2.4 GHz) in Active Mode
- Work Mode | RF Condition | Description | Peak (mA)
- TX | 802.11b, 1 Mbps, DSSS @ 20dBm | — | 339
- RX | 802.11g, 54 Mbps, OFDM @ 17dBm | — | 270
- TX | 802.11n, HT20, MCS7 @ 17dBm | — | 271
- RX | 802.11n, HT40, MCS7 @ 16dBm | — | 259
- RX | 802.11ax, MCS9 @ 15dBm | — | 246
- TX | 802.11b/g/n, HT20 | — | 99
- RX | 802.11n, HT40 | — | 107
- RX | 802.11ax, HE20 | — | 100

Footer: Espressif Systems ESP32-C5 Series Datasheet v1.0 Submit Documentation Feedback Page Number: 68