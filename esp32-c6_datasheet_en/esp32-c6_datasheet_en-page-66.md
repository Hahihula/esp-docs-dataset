**Title: Electrical Characteristics**

---

### Table 5-5. ADC Characteristics

| Symbol | Min   | Max   | Unit |
|--------|-------|-------|------|
| DNL (Differential nonlinearity) \(1\) | -8    | 12    | LSB  |
| INL (Integral nonlinearity)          | -10   | 10    | LSB  |
| Sampling rate                         | —     | 100   | kSPS \(2\) |

**Note:** To get better DNL results, you can sample multiple times and apply a filter, or calculate the average value. \(2\) kSPS means kilo samples-per-second.

The calibrated ADC results after hardware calibration and software calibration are shown in Table 5-6. For higher accuracy, you may implement your own calibration methods.

---

### Table 5-6. ADC Calibration Results

| Parameter | Description                                                                                   | Min   | Max   | Unit |
|-----------|----------------------------------------------------------------------------------------------|-------|-------|------|
| Total error | ATTENTION10, effective measurement range of 0 ~ 1000                                        | -12   | 12    | mV   |
|            | ATTENTION11, effective measurement range of 0 ~ 1300                                          | -12   | 12    | mV   |
| Total error | ATTENTION12, effective measurement range of 0 ~ 1900                                          | -23   | 23    | mV   |
|            | ATTENTION13, effective measurement range of 0 ~ 3300                                          | -40   | 40    | mV   |

**Note:** The above ADC measurement range and accuracy are applicable to chips manufactured on and after the Date Code \(212023\) on shielding cases, or assembled on and after the D/C 1 and D/C 2 \(2321\) on bar-code labels. For chips manufactured or assembled earlier than these date codes, please ask our sales team to provide the actual range and accuracy according to batch.

For details of Date Code and D/C, please refer to Espressif Chip Packaging Information.

---

**Title: Current Consumption Characteristics**

### 5.6

#### Subtitle: Current Consumption in Active Mode \(5.6.1\)

The current consumption measurements are taken with a 3.3 V supply at 25 °C ambient temperature.
- TX current consumption is rated at a 100% duty cycle.

RX current consumption is rated when the peripherals are disabled and the CPU idle.

---

### Table 5-7. Current Consumption for Wi-Fi (2.4 GHz) in Active Mode

| Work Mode | RF Condition       | Description                          | Peak (mA) |
|-----------|--------------------|--------------------------------------|------------|
|           |                    |                                      |            |
| TX       | 802.11b, 1 Mbps, DSSS @ 21.0 dBm   |                                      | 354        |
|          | 802.11g, 54 Mbps, OFDM @ 19.5 dBm  |                                      | 300        |
|          | 802.11n, HT20, MCS7 @ 18.5 dBm    |                                      | 280        |
| Active (RF working) | 802.11n, HT40, MCS7 @ 18.0 dBm   |                                      | 268        |
|          | 802.11ax, MCS9, @ 16.5 dBm       |                                      | 252        |

---

**Footer:** Espressif Systems  
ESP32-C6 Series Datasheet v1.4

**Note at the bottom of page:**
- Submit Documentation Feedback