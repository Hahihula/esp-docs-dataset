

```markdown
Chapter 9 Low-power Management

GoBack

Figure 9.3-5. Digital System Regulator

9.3.4.2 Low-power Voltage Regulator

ESP32-C3's built-in low-power voltage regulator converts the external power supply (typically 3.3 V) to 1.1 V for RTC power domains. Note when the pin CHIP_PU is at a high level, the low-power voltage regulator cannot be turned off. Otherwise, the low power voltage regulator is off when chip enters Light-sleep and Deep-sleep modes. In this case, the RTC domain is powered by an ultra low-power internal power source.

For the architecture of the ESP32-C3 low-power voltage regulator, see Figure 9.3-6.

Figure 9.3-6. Low-power voltage regulator

9.3.4.3 Brownout Detector

The brownout detector checks the voltage of pins VDD3P3_RTC, VDD3P3_CPU, VDDA1, and VDDA2. If the voltage of these pins drops below the predefined threshold (2.7 V by default), the detector would trigger a signal to shut down some power-consuming blocks (such as LNA, PA, etc.) to allow extra time for the digital system to save and transfer important data.

RTC_CNTL_BROWN_OUT_DET indicates the output level of brown-out detector. This register is low level by
```