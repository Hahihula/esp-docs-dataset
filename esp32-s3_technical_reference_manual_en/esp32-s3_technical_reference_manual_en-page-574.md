**Chapter Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**Section Number and Name:**
10.3-7.

**Figure Caption with Diagram Description:**
Figure 10.3-7. Flash Voltage Regulator

**Body Text:**

1. **Configure XPD_SDIO_REG to select power source to components outside of the digital and RTC:**
   - When the voltage regulator outputs a voltage of 3.3 V or 1.8 V.
   - The configuration is as follows:
     - `RTC_CNTL_SDIO FORCE == 0` and `EFUSE_VDD_SPI_FORCE == 1`
     - `XPD_SDIO_REG` defined by `EFUSE_VDD_SPI_XPD`

2. **Configure SDIO_TIEH to choose between 3.3 V or 1.8 V:**
   - When the voltage regulator outputs a reference voltage of typically 1.8 V.
   - The configuration is as follows:
     - `RTC_CNTL_SDIO FORCE == 0` and `EFUSE_VDD_SPI_FORCE == 1`
     - `XPD_SDIO_REG` defined by `EFUSE_VDD_SPI_XPD`

**Additional Configuration Details:**
- When the chip in inactive mode, `RTC_CNTL_SDIO FORCE == 0` or when it is powered up.
- In sleep modes and `RTC_CNTL_SDIO_REG_PD_EN == 1`, `XPD_SDIO_REG` = 0.

**Configuration of SDIO_TIEH:**
- When both conditions are met:
  - `EFUSE_VDD_SPI_TIEH`
- Otherwise, use `RTC_TIEH = RTC_CNTL_SDIO_TIEH`.

**Subsection Title and Description:**

10.3.4 Brownout Detector

The brownout detector checks the voltage of pins VDDP3P3, VDDP3P3_RTC, and VDDP3P3_CPU.
- If these voltages drop below a predefined threshold (2.7 V by default), it triggers an alarm to shut down some power-consuming blocks like LNA or PA for extra time allowing the digital system to save important data.

The brownout detector has ultra-low power consumption when powered up and is enabled whenever necessary, as per Figure 10.3-8 in ESP32-S3 architecture details.
  
**Footer:**
Espressif Systems
Page number (574)
Submit Documentation Feedback

**Document Reference:** 
ESP32-S3 TRM (Version 1.7)