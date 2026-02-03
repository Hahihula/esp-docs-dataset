**Chapter 2: ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

**2.9.4 RTC I2C (I2C) Register Summary**

The addresses in this section are relative to low-power management base address + 0x0C00 provided in Table 4.3-3 in Chapter 4 System and Memory.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| RTC_I2C_SCL_LOW_REG | Configure the low level width of SCL | 0x0000 | R/W |
| RTC_I2C_SCL_HIGH_REG | Configure the high level width of SCL | 0x0014 | R/W |
| RTC_I2C_SDA_DUTY_REG | Configure the SDA hold time after a negative SCL edge | 0x0018 | R/W |
| RTC_I2C_SCL_START_PERIOD_REG | Configure the delay between the SDA and SCL for start condition (negative edge) | 0x001C | R/W |
| RTC_I2C_SCL_STOP_PERIOD_REG | Configure the delay between SDA and SCL positive edge for a stop condition | 0x0020 | R/W |
| RTC_I2C Control Registers | Transmission setting | 0x0004 | R/W |
| RTC_I2C_STATUS_REG | RTC I2C status | 0x0008 | RO |
| RTC_I2C_TO_REG | Configure RTC I2C timeout | 0x000C | R/W |
| RTC_I2C_SLAVE_ADDR_REG | Configure slave address | 0x0010 | R/W |
| RTC_I2C Interrupt Registers | Clear RTC I2C interrupt | 0x0024 | WO |
| RTC_I2C_INT_RAW_REG | RTC I2C raw interrupt | 0x0028 | RO |
| RTC_I2C_INT_ST_REG | RTC I2C interrupt status | 0x002C | RO |
| RTC_I2C_INT_ENA_REG | Enable RTC I2C interrupt | 0x0030 | R/W |
| RTC_I2C Status Register | RTC I2C read data | 0x0034 | varies |
| RTC_I2C_DATA_REG | RTC I2C Command Registers | 0x0038 | varies |
| RTC_I2C_CMD0_REG | RTC I2C Command 0 | 0x003C | varies |
| RTC_I2C_CMD1_REG | RTC I2C Command 1 | 0x0040 | varies |
| RTC_I2C_CMD2_REG | RTC I2C Command 2 | 0x0044 | varies |
| RTC_I2C_CMD3_REG | RTC I2C Command 3 | 0x0048 | varies |
| RTC_I2C_CMD4_REG | RTC I2C Command 4 | 0x0050 | varies |
| RTC_I2C_CMD5_REG | RTC I2C Command 5 | 0x0054 | varies |
| RTC_I2C_CMD6_REG | RTC I2C Command 6 | 0x0058 | varies |
| RTC_I2C_CMD7_REG | RTC I2C Command 7 | 0x005C | varies |
| RTC_I2C_CMD8_REG | RTC I2C Command 8 | 0x0060 | varies |
| RTC_I2C_CMD9_REG | RTC I2C Command 9 | 0x0064 | varies |
| RTC_I2C_CMD10_REG | RTC I2C Command 10 | 0x0068 | varies |
| RTC_I2C_CMD11_REG | RTC I2C Command 11 | 0x0070 | varies |
| RTC_I2C_CMD12_REG | RTC I2C Command 12 | 0x0074 | varies |
| RTC_I2C_CMD13_REG | RTC I2C Command 13 | 0x0078 | varies |
| RTC_I2C_CMD14_REG | RTC I2C Command 14 | 0x007C | varies |
| RTC_I2C_CMD15_REG | RTC I2C Command 15 | 0x0080 | varies |

**Version register**

---

*Espressif Systems*

*Submit Documentation Feedback*

*ESP32-S3 TRM (Version 1.7)*