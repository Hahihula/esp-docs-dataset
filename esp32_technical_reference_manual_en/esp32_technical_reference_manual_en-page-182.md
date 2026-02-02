**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Figure Caption and Description:**
- Figure 9.3-1 shows the structure of a digital core’s voltage regulator.
- The diagram includes components labeled ESP32, VDD3P3_CPU, VDD3P3_RTC, dbias[2:0], VREF, Digital Core.

**Subsection Title with Subheading and Content:**
9.3.3 Low-Power Voltage Regulator

The built-in low-power voltage regulator can convert the external power supply (typically 3.3V) to 1.1V to support the internal RTC core. To save power, it receives a wide range of external power supply from 1.8V to 3.6V, and supports an adjustable output voltage of 0.90V to 1.25V in normal work mode; a fixed output voltage of about 0.75V both in Deep-sleep mode and Hibernation mode.

**List Items:**
1. When the pin CHIP_PU is at a high level, the low-power voltage regulator cannot be turned off. It should be switched only between normal-work mode and Deep-sleep mode.
2. In normal-work mode, RTC_DBIAS[2:0] can be used to tune the output voltage:
   ```
   VDD_RTC = 0.90 + DBIAS * 0.05V
   ```
3. In Deep-sleep mode, the output voltage of the regulator is fixed at about 0.75V.
4. The current to the RTC core comes from pin VDD3P3_RTC.

**Additional Figure Caption and Description:**
- Figure 9.3-2 shows the structure of a low-power voltage regulator.

**Footer Information:**
Espressif Systems
182 ESP32 TRM (Version 5.6)
Submit Documentation Feedback