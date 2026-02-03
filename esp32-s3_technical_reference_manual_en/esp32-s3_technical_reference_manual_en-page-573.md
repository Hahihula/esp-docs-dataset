**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Titles and Subsections with Content:**

- **10.3.4.1 Digital Voltage Regulator**
  - ESP32-S3’s built-in digital voltage regulator converts the external power supply (typically 3.3 V) to 1.1 V for digital power domains. This regulator is controlled by xpd_dig_reg (see details in Figure 10.3-1). For the architecture of the ESP32-S3 digital voltage regulator, see Figure 10.3-5.

**Figure Caption:**
Figure 10.3-5. Digital Voltage Regulator

- **10.3.4.2 Low-power Voltage Regulator**
  - ESP32-S3’s built-in low-power voltage regulator converts the external power supply (typically 3.3 V) to 1.1 V for RTC power domains. When the pin CHIP_PU is at a high level, the RTC domain is always-on. The low power voltage regulator is off when chip enters Light-sleep and Deep-sleep modes. In this case, the RTC domain is powered by an ultra low-power built-in power supply (This power supply cannot be turned off). For the architecture of the ESP32-S3 low-power voltage regulator, see Figure 10.3-1.

**Figure Caption:**
Figure 10.3-6. Low-power Voltage Regulator

- **10.3.4.3 Flash Voltage Regulator**
  - ESP32-S3’s built-in flash voltage regulator can supply a voltage of 3.3 V or 1.8 V to other components outside of digital and RTC, such as flash. For the architecture of the ESP32-S3 flash voltage regulator, see Figure Espressif Systems

**Footer:**
573
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback