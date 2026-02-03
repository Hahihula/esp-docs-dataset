**Title:**
Chapter 39 On-Chip Sensors and Analog Signal Processing

**GoBack**

---

### Register Description:

#### Register 39.37, SENS_SAR_PERI_CLK_GATE_CONF_REG (0x0104)

| Bit | Name                          |
|-----|-------------------------------|
| 31-28 | Reserved                      |
| 27   | SENS_RTC_I2C_EN             Enable RTC I2C clock. (R/W) |
| 26   | SENS_TSENS_CLK_EN           Enable temperature sensor clock. (R/W) |
| 25   | SENS_SARADC_CLK_EN          Enable SAR ADC clock. (R/W) |
| 24   | SENS_IOMUX_CLK_EN           Enable IO MUX clock. (R/W) |

#### Register 39.38, SENS_SAR_PERI_RESET_CONF_REG (0x0108)

| Bit | Name                          |
|-----|-------------------------------|
| 31-28 | Reserved                      |
| 27   | SENS_COPOWER_RESET          Enable ULP-RISC-V reset. (R/W) |
| 26   | SENS_RTC_I2C_RESET          RTC I2C reset. (R/W) |
| 25   | SENS_TSENS_RESET            Enable SAR ADC reset. (R/W) |
| 24   | SENS_SARADC_RESET           Enable IO MUX reset. (R/W) |

#### Register 39.39, SENS_SAR_TOUCH_STATUSO_REG (0x00A0)

| Bit | Name                          |
|-----|-------------------------------|
| 31-26 | Reserved                      |
| 25   | SENS TOUCH SCAN CURR        Indicates the pin that is being in scan status. (RO) |

---

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)

--- 

*Note: The image contains binary representations for each register, but they are not transcribed here as per instructions.*