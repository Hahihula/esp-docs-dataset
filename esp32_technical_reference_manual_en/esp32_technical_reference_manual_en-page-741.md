**Chapter Title:**
Chapter 31 On-Chip Sensors and Analog Signal Processing

**Note Section:**
PWDET/PKDET controller is for Wi-Fi internal use only. If Wi-Fi module is using the SAR ADC2, users can not measure the analog signal from the pins using SAR ADC2. After SAR ADC2 is released by Wi-Fi, users can use SAR ADC2 normally.

**Figure Caption and Diagram:**
- **Figure 31.3-1:** SAR ADC Depiction
  - The diagram shows an Analog Domain with inputs leading to a Low Noise Amplifier (SAR ADC1), which then connects to the RTC Domain's RTC ADC1 Controller, Digital Domain’s Digital ADC1 Controller via DMA and Power/Peak Detect Controller.
  
**Subsection Title:**
31.3.2 Features

**List of Features:**
- Two SAR ADCs, with simultaneous sampling and conversion
- Up to five SAR ADC controllers for different purposes (e.g., high performance, low power or PWDET / PKDET).
- Up to 18 analog input pads
- 12-bit, 11-bit, 10-bit, 9-bit configurable resolution
- DMA support (available on one controller)
- Multiple channel-scanning modes (available on two controllers)
- Operation during Deep-sleep (available on one controller)
- Controlled by a ULP coprocessor (available on two controllers)

**Subsection Title:**
31.3.3 Outline of Function

**Body Text for Subsection 31.3.3:**
The SAR ADC module’s major components, and their interconnections, are shown in Figure 31.3-2.

**Footer Information:**
Espressif Systems
741 ESP32 TRM (Version 5.6)
Submit Documentation Feedback