**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Figure Caption and Diagrams:**
- Figure 9.3-3 shows a Flash Voltage Regulator.
- The diagram includes components labeled ESP32, VDD3P3_RTC, tieh, drefm, drefl, VREF, VDD_SDIO.

**Section Title (Subsection):**
9.3.5 Brownout Detector

**Body Text:**
The brownout detector checks the voltage of pin VDD3P3_RTC. If the voltage drops rapidly and becomes too low, the detector would trigger a signal to shut down some power-consuming blocks (such as LNA, PA, etc.) to allow extra time for the digital block to save and transfer important data. The power consumption of the detector is ultra low. It remains enabled whenever the chip is powered on, with an adjustable trigger level calibrated around 2.5V.

**List:**
1. As the output of the brownout detector, RTC_CNTL_BROWN_OUT_DET goes high when the voltage of pin VDD3P3_RTC is lower than the threshold value.
2. RTC_CNTL_DBROWN_OUT_THRES[2:0] is used to tune the threshold voltage, which is usually calibrated around 2.5V.

**Figure Caption and Diagrams Continued:**
- Figure 9.3-4 shows a Brownout Detector with components labeled ESP32, VREF, thres[2:0], and brownout detected signal.
  
**Section Title (Subsection):**
9.3.6 RTC Module

**Body Text:**
The RTC module is designed to handle the entry into, and exit from, the low-power mode, and control the clock sources, PLL, power switch and isolation cells to generate power-gating, clock-gating, and reset signals.

As for the low-power management, RTC is composed of the following modules (see Figure 9.3-5):

**Footer:**
Espressif Systems
184 ESP32 TRM (Version 5.6)
Submit Documentation Feedback