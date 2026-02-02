**Chapter Title:**
Chapter 9 Low-Power Management (RTC_CNTL)

**Figure Caption and Diagram Description:**
- **Figure:** Figure 9.3-2 shows a block diagram of the low-power voltage regulator.
- The components in the figure include ESP32, VDD3P3_RTC connected to dbias[2:0], an operational amplifier with VREF as its positive input reference.

**Section Title and Subtitle:**
9.3.4 Flash Voltage Regulator

**Body Text:**
The built-in flash voltage regulator can supply a voltage of 3.3V or 1.8V to other devices (flash, for example) in the system, with a maximum output current of 40 mA.

- **List Item:** When XPD_SDIO_VREG == 1, the regulator outputs a voltage of 3.3V or 1.8V; when XPD_SDIO_VREG == 0, the output is high-impedance and in this case, the voltage is provided by the external power supply.
  
- **List Item:** When SDIO_TIEH == 1, the regulator shorts pin VDD_SDIO to pin VDD3P3RTC. The regulator then outputs a voltage of 3.3V which is the voltage of pin VDD3P3_RTC. When SDIO_TIEH == 0, the inner loop ties the regulator output to the voltage of VREF, which is typically 1.8V.

- **List Item:** DREFH_SDIO, DREFM_SDIO and DREFL_SDIO could be used to tune the reference voltage VREF slightly. However, it is recommended that users do not change the value of these registers since they may affect the stability of the inner loop.
  
- **List Item:** When the regulator output is 3.3V or 1.8V, the output current comes from pin VDD3P3_RTC.

**Additional Information:**
Figure 9.3-3 shows the structure of a flash voltage regulator.

**Footer Text and Navigation Links:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)