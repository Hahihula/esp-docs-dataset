**Title:**
Chapter 10 Low-power Management (RTC_CNTL)

**GoBack**

**Register Information and Description:**

- **Register Name:** RTC_CNTL_RTC_TIMER5_REG (0xC02C)
  - **Description:** Sets the minimal sleep cycles (using the RTC slow clock). (R/W)

- **Register Name:** RTC_CNTL_RTC_ANA_CONF_REG (0xC034)
  - **Fields Description:**
    - **RTC_CNTL_I2C_RESET_POR FORCE_PD** Set this bit to FPD SLEEP_I2CPOR. (R/W)
    - **RTC_CNTL_I2C_RESET_POR FORCE PU** Set this bit to FPU SLEEP_I2CPOR. (R/W)
    - **RTC_CNTL_GLITCH_RST_EN** Set this bit to enable a reset when the system detects a glitch. (R/W)

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)