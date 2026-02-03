**Chapter Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

---

**Table of ADC Selections**

| Pin/Signal | Channel | ADC Selection |
|-------------|---------|---------------|
| GPIO18      |         |               |
| GPIO19      |         |               |
| GPIO20      |         |               |

**Section Title: 39.3.5 ADC Conversion and Attenuation**

When the SAR ADCs convert an analog voltage, the resolution (12-bit) of the conversion spans a voltage range from 0 mV to \( V_{ref} \). Here, \( V_{ref} \) is the SAR ADC's internal reference voltage (\( 1100 \text{mV} \) by design). The output value of the conversion (data) is mapped to analog voltage \( V_{data} \) using the following formula:

\[ V_{data} = \frac{V_{ref}}{4095} \times data \]

In order to convert voltages larger than \( V_{ref} \), input signals can be attenuated before being input into the SAR ADCs. The attenuation can be configured to 0 dB, 2.5 dB, 6 dB, and 12 dB.

**Section Title: 39.3.6 RTC ADC Controller**

The RTC ADC1/2 controllers are powered in the RTC power domain; thus allowing the SAR ADCs to conduct measurements at a low frequency with minimal power consumption. The overview of a single RTC ADC controller's function is shown in Figure **39.3-3**.

![Figure 39.3-3: RTC ADC Controller Overview](image-description-or-link)

Conversion is triggered by \( SENS_SAR_MEASn_START_SAR \), and then the conversion result is stored to \( SENS_SAR_MEASn_DATA_SAR \).

The RTC ADC1/2 controllers are intertwined with the ULP coprocessor, as the ULP coprocessor has a built-in instruction to start an ADC conversion. In many cases, the controllers need to cooperate with the ULP coprocessor; for example,

- When the controllers periodically monitor a channel during Deep-sleep, ULP coprocessor is the only source to trigger ADC sampling by configuring RTC registers.
- Continuous scanning or DMA is not supported by the controllers. However, it is possible with the help of ULP coprocessor to scan channels continuously in a sequence.

There are two ways to set the sampling channels:

---

**Footer:**
Espressif Systems  
1469  
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)