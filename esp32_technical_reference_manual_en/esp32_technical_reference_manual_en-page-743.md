**Chapter Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**GoBack Link:** GoBack

**Body Text:**

There are five ADC controllers in ESP32: RTC ADC1 CTRL, RTC ADC2 CTRL, DIG ADC1 CTRL, DIG ADC2 CTRL and PWDET CTRL. The differences between them are summarized in Table 31.3-2.

**Table Title:**
Table 31.3-2. ESP32 SAR ADC Controllers

| DAC | RTC ADC1 | RTC ADC2 | DIG ADC1 | DIG ADC2 | PWDET |
|-----|----------|----------|----------|----------|-------|
| Y   | -        | -        | -        | -        | -     |
| Support deep sleep | Y       | -        | -        | -        | -     |
| ULP coprocessor | Y      | -        | -        | -        | -     |
| PWDET/PKDET | -    | -        | -        | -        | Y     |
| DMA  | -      | -        | -        | -        | -     |

**Subsection Title:**
31.3.4 RTC SAR ADC Controllers

The purpose of SAR ADC controllers in the RTC power domain – RTC ADC1 CTRL and RTC ADC2 CTRL – is to provide ADC measurement with minimal power consumption in a low frequency.

The outline of a single controller’s function is shown in Figure 31.3-3. For each controller, the start of analog-to-digital conversion can be triggered by register SENS_SAR_MEASn_START_SAR. The measurement's result can be obtained from register SENS_SAR_MEASn_DATA_SAR.

**Figure Title:**
Figure 31.3-3. RTC SAR ADC Outline of Function

The controllers are intertwined with the ULP coprocessor, as the ULP coprocessor has a built-in instruction to start an ADC measurement. In many cases, the controllers need to cooperate with the ULP coprocessor,

e.g.:
- when periodically monitoring a channel during deep sleep, where the ULP coprocessor is the only trigger source during this mode;
- when scanning channels continuously in a sequence. Continuous scanning or DMA is not supported by the controllers. However, it is possible with the help of the ULP coprocessor.

**Subsection Title:**
31.3.5 DIG SAR ADC Controllers

Compared to RTC SAR ADC controllers, DIG SAR ADC controllers have optimized performance and throughput. Some of their features are:

- High performance; the clock is much faster, therefore, the sample rate is highly increased.
  - **Note:** This text seems incomplete or cut off at "the sample rate is highly increased."

**Footer:**
Espressif Systems  
743  
Submit Documentation Feedback

ESP32 TRM (Version 5.6)