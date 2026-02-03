**Chapter 2: ULP Coprocessor (ULP-FSM, ULP-RISC-V)**

- **ULP (ALWAYS_ON) registers:** not reset due to power down of RTC_PERI domain. See Chapter 10 Low-power Management (RTC_CNTL).
- **ULP (RTC_PERI) registers:** reset due to power down of RTC_PERI domain. See Chapter 10 Low-power Management (RTC_CNTL).
- **RTC I2C registers:** I2C related registers, including RTC I2C (RTC_PERI) and RTC I2C (I2C).

**2.9.1 ULP (ALWAYS_ON) Register Summary**

The addresses in this section are relative to low-power management base address provided in Table 4.3-3 in Chapter 4 System and Memory.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **ULP Timer Registers** | Configure the timer | RTC_CNTL_ULP_CP_TIMER_REG | 0x00FC varies |
| | Configure sleep cycle of the timer | RTC_CNTL_ULP_CP_TIMER_1_REG | 0x0134 R/W |
| ULP-FSM Register | ULP-FSM configuration register | RTC_CNTL_ULP_CP_CTRL_REG | 0x0100 R/W |
| **ULP-RISC-V Register** | ULP-RISC-V configuration register | RTC_CNTL_COCPU_CTRL_REG | 0x0104 varies |

**2.9.2 ULP (RTC_PERI) Register Summary**

The addresses in this section are relative to low-power management base address provided in Table 4.3-3 in Chapter 4 System and Memory.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **ULP-RISC-V Registers** | Interrupt raw bit of ULP-RISC-V | SENS_SAR_COCPU_INT_RAW_REG | 0x00E8 RO |
| | Interrupt enable bit of ULP-RISC-V | SENS_SAR_COCPU_INT_ENA_REG | 0x00EC R/W |
| | Interrupt status bit of ULP-RISC-V | SENS_SAR_COCPU_INT_ST_REG | 0x00FO RO |
| | Interrupt clear bit of ULP-RISC-V | SENS_SAR_COCPU_INT_CLR_REG | 0x00F4 WO |

**2.9.3 RTC I2C (RTC_PERI) Register Summary**

The addresses in this section are relative to low-power management base address + 0x0800 provided in Table 4.3-3 in Chapter 4 System and Memory.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **RTC I2C Controller Register** | Configure RTC I2C transmission | SENS_SAR_I2C_CTRL_REG | 0x0058 R/W |
| **RTC I2C Slave Address Registers** | Configure slave addresses 0-1 of RTC I2C | SENS_SAR_SLAVE_ADDR1_REG | 0x0040 R/W |
| | Configure slave addresses 2-3 of RTC I2C | SENS_SAR_SLAVE_ADDR2_REG | 0x0044 R/W |
| | Configure slave addresses 4-5 of RTC I2C | SENS_SAR_SLAVE_ADDR3_REG | 0x0048 R/W |
| | Configure slave addresses 6-7 of RTC I2C | SENS_SAR_SLAVE_ADDR4_REG | 0x004C R/W |

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Page number: 332

[Submit Documentation Feedback](#)