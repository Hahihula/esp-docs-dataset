

```markdown
| No.| Chapter| Interrupt Source| Interrupt Source Mapping Register| Bit| Interrupt Status Register Name|
|----:|--------|------------------|-----------------------------------|----:|-------------------------------|
| 32 | n/a    | reserved         | reserved                          |   0|                               |
| 33 | System Registers | HP_PERI_TIMEOUT_INTR | INTMTX_COREO_HP_PERI_TIMEOUT_INTR_MAP_REG |   1|                               |
| 34 | n/a    | reserved         | reserved                          |   2|                               |
| 35 | Permission Control (PMS) | HP_APM_MO_INTR | INTMTX_COREO_HP_APM_MO_INTR_MAP_REG |   3|                               |
| 36 | Permission Control (PMS) | HP_APM_M1_INTR | INTMTX_COREO_HP_APM_M1_INTR_MAP_REG |   4|                               |
| 37 | Permission Control (PMS) | HP_APM_M2_INTR | INTMTX_COREO_HP_APM_M2_INTR_MAP_REG |   5|                               |
| 38 | Permission Control (PMS) | HP_APM_M3_INTR | INTMTX_COREO_HP_APM_M3_INTR_MAP_REG |   6|                               |
| 39 | Permission Control (PMS) | LP_APMO_INTR     | INTMTX_COREO_LP_APMO_INTR_MAP_REG  |   7|                               |
| 40 | SPI Controller (SPI) | MSPI_INTR        | INTMTX_COREO_MSPI_INTR_MAP_REG     |   8|                               |
| 41 | I2S Controller (I2S)| I2S_INTR         | INTMTX_COREO_I2S_MAP_REG           |   9|                               |
| 42 | UART Controller (UART_LP_UART_UHCI) | UHClO_INTR | INTMTX_COREO_UHCIO_INTR_MAP_REG    |  10|                               |
| 43 | UART Controller (UART_LP_UART_UHCI) | UARTO_INTR   | INTMTX_COREO_UARTO_INTR_MAP_REG    |  11|                               |
| 44 | UART Controller (UART_LP_UART_UHCI) | UART1_INTR   | INTMTX_COREO_UART1_INTR_MAP_REG    |  12|                               |
| 45 | LED PWM Controller (LEDC)| LEDC_INTR      | INTMTX_COREO_LEDC_INTR_MAP_REG     |  13|                               |
| 46 | Two-wire Automotive Interface (TWAI) | TWAO_INTR   | INTMTX_COREO_TWAO_INTR_MAP_REG     |  14|                               |
| 47 | Two-wire Automotive Interface (TWAI) | TWA1_INTR    | INTMTX_COREO_TWA1_INTR_MAP_REG     |  15| INTMTX_COREO_INT_STATUS_1_REG|
| 48 | USB Serial/JTAG Controller (USB_SERIAL_JTAG)| USB_SERIAL_JTAG_INTR | INTMTX_COREO_USB_INTR_MAP_REG      |  16|                               |
| 49 | Remote Control Peripheral (RMT) | RMT_INTR        | INTMTX_COREO_RMT_INTR_MAP_REG      |  17|                               |
| 50 | I2C Controller (I2C)| I2C_EXTO_INTR    | INTMTX_COREO_I2C_EXTO_INTR_MAP_REG |  18|                               |
| 51 | Timer Group (TIMG)   | TGO_TO_INTR      | INTMTX_COREO_TGO_TO_INTR_MAP_REG   |  19|                               |
| 52 | n/a    | reserved         | reserved                          |  20|                               |
| 53 | Timer Group (TIMG)| TGO_WDT_INTR     | INTMTX_COREO_TGO_WDT_INTR_MAP_REG  |  21|                               |
| 54 | Timer Group (TIMG)| TG1_TO_INTR      | INTMTX_COREO_TG1_TO_INTR_MAP_REG   |  22|                               |
| 55 | n/a    | reserved         | reserved                          |  23|                               |
| 56 | Timer Group (TIMG)| TG1_WDT_INTR     | INTMTX_COREO_TG1_WDT_INTR_MAP_REG  |  24|                               |
| 57 | System Timer (SYSTIMER) | SYSTIMER_TARGET_TO_INTR | INTMTX_COREO_SYSTIMER_TARGET_TO_INTR_MAP_REG | 25|                               |
| 58 | System Timer (SYSTIMER)| SYSTIMER_TARGET1_INTR | INTMTX_COREO_SYSTIMER_TARGET1_INTR_MAP_REG | 26|                               |
| 59 | System Timer (SYSTIMER)| SYSTIMER_TARGET2_INTR | INTMTX_COREO_SYSTIMER_TARGET2_INTR_MAP_REG | 27|                               |
| 60 | On-Chip Sensor and Analog Signal Processing | APB_ADC_INTR | INTMTX_COREO_APB_ADC_INTR_MAP_REG   | 28|                               |
| 61 | Motor Control PWM (MCPWM)| PWM_INTR       | INTMTX_COREO_PWM_INTR_MAP_REG      | 29|                               |
| 62 | Pulse Count Controller (PCNT) | PCNT_INTR     | INTMTX_COREO_PCNT_INTR_MAP_REG     | 30|                               |
| 63 | Parallel IO Controller (PARL_IO)| PARL_IO_INTR | INTMTX_COREO_PARL_IO_INTR_MAP_REG   | 31|                               |
```