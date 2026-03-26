
```markdown
| No. | Chapter                  | Interrupt Source                     | Interrupt Source Mapping Register                                                                                   | Bit | Interrupt Status Register Name |
|-----|--------------------------|--------------------------------------|--------------------------------------------------------------------------------------------------------------------|-----|--------------------------------|
| 0   | RTC Timer                | LP_RTC_INTR                          | COREx_LP_RTC_INT_MAP_REG                                      | 0   |                                |
| 1   | Watchdog Timers (WDT)    | LP_WDT_INTR                          | COREx_LP_WDT_INT_MAP_REG                                      | 1   |                                |
| 2   | RTC Timer                | LP_TIMER_REG_O_INTR                 | COREx_LP_TIMER_REG_O_INT_MAP_REG                              | 2   |                                |
| 3   | RTC Timer                | LP_TIMER_REG_1_INTR                 | COREx_LP_TIMER_REG_1_INT_MAP_REG                              | 3   |                                |
| 4   | LP Mailbox               | MB_LP_INTR                           | COREx_MB_LP_INT_MAP_REG                                       | 4   |                                |
| 5   | LP Mailbox               | MB_HP_INTR                           | COREx_MB_HP_INT_MAP_REG                                       | 5   |                                |
| 6   | Low-Power Management     | PMU_REG_O_INTR                       | COREx_PMU_REG_O_INT_MAP_REG                                   | 6   |                                |
| 7   | Low-Power Management     | PMU_REG_1_INTR                       | COREx_PMU_REG_1_INT_MAP_REG                                   | 7   |                                |
| 8   | Brown-out Detector       | LP_ANAPERI_INTR                      | COREx_PMU_REG_O_INT_MAP_REG                                   | 8   |                                |
| 9   | ADC Controller (ADC)     | LP_ADC_INTR                          | COREx_PMU_REG_O_INT_MAP_REG                                   | 9   |                                |
| 10  | GPIO Matrix and IO MUX   | LP_GPIO_INTR                         | COREx_LP_GPIO_INT_MAP_REG                                     | 10  |                                |
| 11  | I2C Controller (I2C)     | LP_I2C_INTR                          | COREx_LP_I2C_INT_MAP_REG                                      | 11  |                                |
| 12  | I2S Controller (I2S)     | LP_I2S_INTR                          | COREx_LP_I2S_INT_MAP_REG                                      | 12  |                                |
| 13  | SPI Controller (SPI)     | LP_SPI_INTR                          | COREx_LP_SPI_INT_MAP_REG                                      | 13  |                                |
| 14  | Touch Sensor (TOUCH)     | LP_TOUCH_INTR                        | COREx_LP_TOUCH_INT_MAP_REG                                    | 14  |                                |
| 15  | Temperature Sensor (TSENS)| LP_TSSENS_INTR                       | COREx_LP_TSSENS_INT_MAP_REG                                   | 15  | COREx_INTR_STATUS_REG_O_REG   |
| 16  | UART Controller (UART)   | LP_UART_INTR                         | COREx_LP_UART_INT_MAP_REG                                     | 16  |                                |
| 17  | eFuse Controller (EFUSE) | LP_EFUSE_INTR                        | COREx_LP_EFUSE_INT_MAP_REG                                    | 17  |                                |
| 18  | Low-Power CPU            | LP_SW_INTR                           | COREx_LP_SW_INT_MAP_REG                                       | 18  |                                |
| 19  | System Registers (SYSREG)| LP_SYSREG_INTR                       | COREx_LP_SYSREG_INT_MAP_REG                                   | 19  |                                |
| 20  | Key Manager              | LP_HUK_INTR                          | COREx_LP_HUK_INT_MAP_REG                                      | 20  |                                |
| 21  | System Registers (SYSREG)| SYS_ICM_INTR                         | COREx_SYS_ICM_INT_MAP_REG                                     | 21  |                                |
| 22  | USB Serial/JTAG Controller (USB_SERIAL_JTAG) | USB_DEVICE_INTR | COREx_USB_DEVICE_INT_MAP_REG                                 | 22  |                                |
| 23  | SD/MMC Host Controller (SDHOST) | SDIO_HOST_INTR                   | COREx_SDIO_HOST_INT_MAP_REG                                   | 23  |                                |
| 24  | GDMA Controller (GDMA-AHB, GDMA-AXI) | GDMA_INTR                       | COREx_GDMA_INT_MAP_REG                                         | 24  |                                |
| 25  | SPI Controller (SPI)     | SPI2_INTR                            | COREx_SPI2_INT_MAP_REG                                         | 25  |                                |
| 26  | SPI Controller (SPI)     | SPI3_INTR                            | COREx_SPI3_INT_MAP_REG                                         | 26  |                                |
| 27  | I2S Controller (I2S)     | I2SO_INTR                            | COREx_I2SO_INT_MAP_REG                                         | 27  |                                |
| 28  | I2S Controller (I2S)     | I2S1_INTR                            | COREx_I2S1_INT_MAP_REG                                         | 28  |                                |
| 29  | I2S Controller (I2S)     | I2S2_INTR_O                           | COREx_I2S2_INT_MAP_REG                                         | 29  |                                |
| 30  | UART Controller (UART)   | UHCIO_INTR                           | COREx_UHCIO_INT_MAP_REG                                        | 30  |                                |
| 31  | UART Controller (UART)   | UARTO_INTR                           | COREx_UARTO_INT_MAP_REG                                       | 31  |                                |
```