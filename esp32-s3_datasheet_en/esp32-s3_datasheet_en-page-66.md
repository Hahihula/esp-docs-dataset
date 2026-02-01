**Title: Electrical Characteristics**

---

### **5.5 ADC Characteristics**

The measurements in this section are taken with an external 100 nF capacitor connected to the ADC, using DC signals as input, and at an ambient temperature of 25 °C with disabled Wi-Fi.

#### Table 5-5. ADC Characteristics

| Symbol | Min   | Max   | Unit |
|--------|-------|-------|------|
| DNL (Differential nonlinearity) \(1\) | -4    | 4     | LSB  |
| INL (Integral nonlinearity)          | -8    | 8     | LSB  |
| Sampling rate                         | —     | 100   | kSPS \(2\) |

**Note:** To get better DNL results, you can sample multiple times and apply a filter, or calculate the average value.

\(2\) kSPS means kilo samples-per-second

The calibrated ADC results after hardware calibration and software calibration are shown in Table 5-6. For higher accuracy, you may implement your own calibration methods.

#### Table 5-6. ADC Calibration Results

| Parameter | Description                                   | Min   | Max   | Unit |
|-----------|-----------------------------------------------|-------|-------|------|
| ATTEN0    | effective measurement range of \(0 \sim 850\) | -5    | 5     | mV   |
| ATTEN1    | effective measurement range of \(0 \sim 1100\) | -6    | 6     | mV   |
| Total error |ATTEN2, effective measurement range of \(0 \sim 1600\)|-10|10|mV|
| ATTEN3    | effective measurement range of \(0 \sim 2900\) | -50   | 50   | mV   |

---

### **5.6 Current Consumption**

#### Subsection: 5.6.1 Current Consumption in Active Mode

The current consumption measurements are taken with a 3.3 V supply at \(25 °C\) ambient temperature.

TX current consumption is rated at a 100% duty cycle.
RX current consumption is rated when the peripherals are disabled and the CPU idle.

#### Table 5-7. Current Consumption for Wi-Fi (2.4 GHz) in Active Mode

| Work Mode | RF Condition           | Peak (mA) |
|-----------|------------------------|-----------|
| TX        | 802.11b, 1 Mbps, @21 dBm | 340       |
|           | 802.11g, 54 Mbps, @19 dBm | 291      |
|           | 802.11n, HT20, MCS7, @18.5 dBm | 283   |
|           | 802.11n, HT40, MCS7, @18 dBm    | 286     |
| RX        | 802.11b/g/n, HT20       | 88        |
|           | 802.11n, HT40          | 91        |

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

ESP32-S3 Series Datasheet v2.1
Page number at the bottom of page is not provided in text but can be inferred as "66" based on common document structure conventions for datasheets and manuals, especially when there are multiple pages referenced within a section or chapter.

(Note: The actual footer content may vary slightly depending on how it appears visually.)