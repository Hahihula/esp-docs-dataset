**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Figure Caption and Diagram Description:**
- **Figure 9.2-1:** ESP32 Power Control

**Section Titles with Subsections:**

- **9.3 Functional Description**
  - **9.3.1 Overview**
    The low-power management unit includes voltage regulators, a power controller, power switch cells, power domain isolation cells, etc. Figure 9.2-1 shows the high-level architecture of ESP32’s low-power management.

  - **9.3.2 Digital Core Voltage Regulator**
    The built-in voltage regulator can convert the external power supply (typically 3.3V) to 1.1V to support the internal digital core. It receives a wide range of external power supply from 1.8V to 3.6V, and provides an output voltage from 0.90V to 1.25V.
      - When XPD_DIG_REG == 1, the regulator outputs a 1.1V voltage and the digital core is able to run; when XPD_DIG_REG == 0, both the regulator and the digital core stop running.

**Additional Information:**
- DIG_REG_DBIAS[2:0] tunes the supply voltage of the digital core:
  - VDD_DIG = 0.90 + DBIAS * 0.05V
- The current to the digital core comes from pin VDD3P3_CPU and pin VDD3P3_RTC.

**Footer Information:**
Espressif Systems  
Page number: 181  
Document version: ESP32 TRM (Version 5.6)  

**Navigation Link:** 
GoBack

**Feedback Option:**
Submit Documentation Feedback