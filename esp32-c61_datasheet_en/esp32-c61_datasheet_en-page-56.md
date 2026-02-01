**Title: Electrical Characteristics**

---

### **5.3 VDD_SPI Output Characteristics**

**Table Title:** Table 5-3. VDD_SPI Internal and Output Characteristics

| Parameter | Description | Typ | Unit |
|-----------|-------------|-----|------|
| R\_SPI    | VDD\_SPI powered by VDD3P3\_RTC via R\_SPI for 3.3 V flash/PSRAM | Ω | - |
|           | See in conjunction with Section **2.5.2 Power Scheme**. |   |     |
|           | VDD3P3\_RTC must be more than VDD\_flash\_min + I\_flash\_max \* R\_SPI; where |   |     |
|           | - VDD\_flash\_min – minimum operating voltage of flash/PSRAM |  |    |
|           | - I\_flash\_max – maximum operating current of flash/PSRAM |  |    |

---

### **5.4 ADC Characteristics**

The measurements in this section are taken with an external 100 nF capacitor connected to the ADC, using DC signals as input, and at an ambient temperature of 25 °C with disabled Wi-Fi.

**Table Title:** Table 5-4. ADC Characteristics

| Symbol | Min | Max | Unit |
|--------|-----|-----|------|
| DNL (Differential nonlinearity) | -5 | 5 | LSB |
| INL (Integral nonlinearity) | -5 | 5 | LSB |
| Sampling rate | – | 2000 kSPS^2 |   |

1. To get better DNL results, you can sample multiple times and apply a filter, or calculate the average value.
2. kSPS means kilo samples-per-second.

The calibrated ADC results after hardware calibration and software calibration are shown in Table **5-5**. For higher accuracy, you may implement your own calibration methods.

---

### **Table Title:** Table 5-5. ADC Calibration Results

| Parameter | Description | Min | Max | Unit |
|-----------|-------------|-----|-----|------|
| ATTENTION10, effective measurement range of 0 ~ 1000 | –10 to +10 mV | -10 | 10 | mV |
| ATTENTION11, effective measurement range of 0 ~ 1300 | –10 to +10 mV | -10 | 10 | mV |
| ATTENTION12, effective measurement range of 0 ~ 1900 | –12 to +12 mV | -12 | 12 | mV |
| ATTENTION13, effective measurement range of 0 ~ 3300 | –15 to +15 mV | -15 | 15 | mV |

---

### **5.5 Current Consumption Characteristics**

#### **5.5.1 Current Consumption in Active Mode**

The current consumption measurements are taken with a 3.3 V supply at 25 °C ambient temperature.

TX current consumption is rated at a 100% duty cycle.
RX current consumption is rated when the peripherals are disabled and the CPU idle.

Espressif Systems

---

ESP32-C61 Series Datasheet v0.5
Page number: **56**