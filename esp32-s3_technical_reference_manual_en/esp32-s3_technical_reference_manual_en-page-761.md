**Title:**
Register 15.50, PMS_CORE_0_PIF_PMS CONSTRAINT_n_REG (n: 1-8) (0x0128 + 4*n)

**Body Text with Table and Descriptions:**

| Register | Description |
|----------|-------------|
| 31       | PMS_CORE_0_PIF_PMS_CONSTRAIN_WORLD_O_UART1 |
| 30       | PMS_CORE_0_PIF_PMS_CONSTRAIN_WORLD_O_UART2 |
| ...      | ...         |
| 0        | Reset |

**Descriptions:**

- **PMS_CORE_0_PIF_PMS CONSTRAIN_WORLD_O_UART**: Configures CPUO’s permission to access UART0 from the Secure World. (R/W)
- **PMS_CORE_0_PIF_PMS CONSTRAIN_WORLD_O_GOSPI_1**: Configures CPUO’s permission to access SPI1 from the Secure World. (R/W)
- **PMS_CORE_0_PIF_PMS CONSTRAIN_WORLD_O_GOSPI_0**: Configures CPUO’s permission to access SPI0 from the Secure World. (R/W)
- **PMS_CORE_0_PIF_PMS CONSTRAIN_WORLD_O_GPIO**: Configures CPUO’s permission to access GPIO from the Secure World. (R/W)
- **PMS_CORE_0_PIF_PMS CONSTRAIN_WORLD_O_RTC**: Configures CPUO's permission to access eFuse Controller & PMU from the Secure World. (R/W)
- **PMS_CORE_0_PIF_PMS CONSTRAIN_WORLD_O_IO_MUX**: Configures CPUO’s permission to access IO_MUX from the Secure World. (R/W)
- **PMS_CORE_0_PIF_PMS CONSTRAIN_WORLD_O_I2S0**: Configures CPUO’s permission to access I2S0 from the Secure World. (R/W)
- **PMS_CORE_0_PIF_PMS CONSTRAIN_WORLD_O_UART1**: Configures CPUO’s permission to access UART1 from the Secure World. (R/W)

**Footer:**
ESP32-S3 TRM (Version 1.7)