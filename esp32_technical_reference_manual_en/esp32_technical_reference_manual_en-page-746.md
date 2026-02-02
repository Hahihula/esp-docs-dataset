**Title: Chapter 31 On-Chip Sensors and Analog Signal Processing**

- Independent or simultaneous conversion in channels

- Voltage reference from the VDD3P3_RTC pin

- Cosine waveform (CW) generator

- DMA capability

- Start of conversion can be triggered by software or SAR ADC FSM (please refer to the [SAR ADC chapter](#) for more details)

- Can be fully controlled by the ULP coprocessor

A diagram showing the DAC channel’s function is presented in Figure 31.4-1.

**Figure Caption:**
Figure 31.4-1. Diagram of DAC Function

---

**Subtitle: 31.4.3 Structure**

The two 8-bit DAC channels can be configured independently. For each DAC channel, the output analog voltage can be calculated as follows:

- **DACn_OUT = VDD3P3_RTC - PDACn_DAC/255**
  
- VDD3P3_RTC is the voltage on pin VDD3P3_RTC (typically 3.3V).

- PDACn_DAC has multiple sources: CW generator, register RTCIO_PAD_DACn_REG, and DMA.

The start of conversion is determined by register RTCIO_PAD_PDACn_XPD_DAC. The conversion process itself is controlled by software or SAR ADC FSM; see Figure 31.4-1.

---

**Subtitle: 31.4.4 Cosine Waveform Generator**

The cosine waveform (CW) generator can be used to generate a cosine / sine tone. A diagram showing cosine waveform generator’s function is presented in Figure 31.4-2.

The CW generator has the following features:

- Adjustable frequency

---

**Footer:**
Espressif Systems  
746  
ESP32 TRM (Version 5.6)  

[Submit Documentation Feedback](#)