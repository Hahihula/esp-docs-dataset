**Title: Chapter 2 ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

**Subtitle: Register 2.9. SENS_SAR_I2C_CTRL_REG (0x0058)**

---

### Table of Registers:
- **SENS_SAR_I2C_START FORCE**
- **SENS_SAR_I2C_START**
- **SENS_SAR_I2C_WR_EN**
- **SENS_SAR_I2C_WDATA**
- **SENS_SAR_I2C_CTRL_REG ADDR**
- **SENS_SAR_I2C_SLAVE_ADDR1_10BIT_EN**

---

### Register Details:
- **Register 2.9: SENS_SAR_I2C_CTRL_REG (0x0058)**

| Bit | Description |
|-----|-------------|
| 31 to 26 | Reserved |
| 19, 18 | SENS_SAR_I2C_SLAVE_ADDR1_10BIT_EN |
| 11 to 9 | SENS_SAR_I2C_CTRL_REG ADDR |
| 0 (Reset) | Reset |

---

### Description of Bits:
- **SENS_SAR_I2C_SLAVE_ADDR** Configures the slave address. (R/W)
- **SENS_SAR_I2C_SLAVE_ADDR_10BIT_EN** Configures whether to expand the slave address to 10 bits.
  - `0`: Not expand
  - `1`: Expand

---

### Additional Registers:
- **SENS_SAR_I2C_REG_ADDR** Configures the register address. (R/W)
- **SENS_SAR_I2C_WDATA** Configures the data to write. (R/W)
- **SENS_SAR_I2C_WR_EN** Configures whether to use write command.
  - `0`: Use read command
  - `1`: Use write command

---

### Start Register:
- **SENS_SAR_I2C_START FORCE**
  - Starts RTC I2C; active only when SENS_SAR_I2C_START FORCE = 1. (R/W)
- **SENS_SAR_I2C_START FORCE** 
  - `0`: RTC I2C started by FSM
  - `1`: RTC I2C started by software

---

### Register 2.10: SENS_SAR_SLAVE_ADDR1_REG (0x0040)

| Bit | Description |
|-----|-------------|
| 31 to 26 | Reserved |
| 21, 20 | SENS_I2C_SLAVE_ADDR1 |
| 11 to 10 | SENS_I2C_SLAVE_ADDR0 |

---

### Additional Registers:
- **SENS_I2C_SLAVE_ADDR1** RTC I2C slave address. (R/W)
- **SENS_I2C_SLAVE_ADDR0** RTC I2C slave address O. (R/W)

---

**Footer:**
Espressif Systems  
341 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback