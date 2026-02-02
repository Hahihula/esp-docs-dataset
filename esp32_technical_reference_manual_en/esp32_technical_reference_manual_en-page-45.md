**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**Section Header:**
1.7 Register Summary

**Subsection Header and Content:**

#### 1.7.1 SENS_ULP Address Space

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **ULP Timer cycles select** |  |  |  |
| SENS_ULP_CP_SLEEP_CYCO_REG | Timer cycles setting 0 | 0x3FF4881B | R/W |
| SENS_ULP_CP_SLEEP_CYC1_REG | Timer cycles setting 1 | 0x3FF4881C | R/W |
| SENS_ULP_CP_SLEEP_CYC2_REG | Timer cycles setting 2 | 0x3FF48820 | R/W |
| SENS_ULP_CP_SLEEP_CYC3_REG | Timer cycles setting 3 | 0x3FF48824 | R/W |
| SENS_ULP_CP_SLEEP_CYC4_REG | Timer cycles setting 4 | 0x3FF48828 | R/W |

**Subsection Header:**
RTC I2C slave address select

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| SENS_SAR_SLAVE_ADDR1_REG | I2C addresses O and 1 | 0x3FF4883C | R/W |
| SENS_SAR_SLAVE_ADDR2_REG | I2C addresses 2 and 3 | 0x3FF48840 | R/W |
| SENS_SAR_SLAVE_ADDR3_REG | I2C addresses 4 and 5 | 0x3FF48844 | R/W |
| SENS_SAR_SLAVE_ADDR4_REG | I2C addresses 6 and 7, I2C control | 0x3FF48848 | R/W |

**Subsection Header:**
RTC I2C control

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| SENS_SAR_CTRL_REG | I2C control registers | 0x3FF48850 | R/W |

#### 1.7.2 RTC_I2C Address Space

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **RTC I2C control registers** |  |  |  |
| RTC_I2C_CTRL_REG | Transmission setting | 0x3FF48C04 | R/W |
| RTC_I2C_DEBUG_STATUS_REG | Debug status | 0x3FF48C08 | R/W |
| RTC_I2C_TIMEOUT_REG | Timeout setting | 0x3FF48C0C | R/W |
| RTC_I2C_SLAVE_ADDR_REG | Local slave address setting | 0x3FF48C10 | R/W |

**Subsection Header:**
RTC I2C signal setting registers

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| RTC_I2C_SDA_DUTY_REG | Configures the SDA hold time after a negative SCL edge | 0x3FF48C30 | R/W |
| RTC_I2C_SCL_LOW_PERIOD_REG | Configures the low level width of SCL | 0x3FF48C00 | R/W |
| RTC_I2C_SCL_HIGH_PERIOD_REG | Configures the high level width of SCL | 0x3FF48C38 | R/W |
| RTC_I2C_SCL_START_PERIOD_REG | Configures the delay between the SDA and SCL negative edge for a start condition | 0x3FF48C40 | R/W |
| RTC_I2C_SCL_STOP_PERIOD_REG | Configures the delay between the SDA and SCL positive edge for a stop condition | 0x3FF48C44 | R/W |

**Subsection Header:**
RTC I2C interrupt registers - listed only for debugging

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| RTC_I2C_INT_CLR_REG | Clear status of I2C communication events | 0x3FF48C24 | R/W |
| RTC_I2C_INT_EN_REG | Enable capture of I2C communication status events | 0x3FF48C28 | R/W |
| RTC_I2C_INT_ST_REG | Status of captured I2C communication events | 0x3FF48C2C | R/O |

**Footer:**
Note:
Espressif Systems
ESP32 TRM (Version 5.6)