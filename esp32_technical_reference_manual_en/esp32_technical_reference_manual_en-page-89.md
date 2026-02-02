**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**Body Text:**
For the APP_CPU, MMU entry 3200 needs to be set to 0x40 and marked as valid by clearing the 8th bit. Thus, 0x040 is written to MMU entry 3200.

Now, the PRO_CPU and the APP_CPU can access different physical memory regions through the same virtual address.

**Subsection Title:**
4.3.2.3 Peripheral

**Body Text:**
The Peripheral MPU manages the 39 peripheral modules. This MMU can be configured per peripheral to only allow access from a process with a certain PID. The registers to configure this are detailed in Table 4.3-19.

**Table Title:**
Table 4.3-19. MPU for Peripheral

| Peripheral | Authority |
|------------|-----------|
| DPort Register | Access Forbidden |
| AES Accelerator | Access Forbidden |
| RSA Accelerator | Access Forbidden |
| SHA Accelerator | Access Forbidden |
| Secure Boot | Access Forbidden |
| Cache MMU Table | Access Forbidden |
| PID Controller | Access Forbidden |
| UART0 | DPORT_AHBLITE MPU_TABLE_UART_REG |
| SPI1 | DPORT_AHBLITE MPU_TABLE_SPI1_REG |
| SPI0 | DPORT_AHBLITE MPU_TABLE_SPI0_REG |
| GPIO | DPORT_AHBLITE MPU_TABLE_GPIO_REG |
| RTC | DPORT_AHBLITE MPU_TABLE_RTC_REG |
| IO MUX | DPORT_AHBLITE MPU_TABLE_IO_MUX_REG |
| SDIO Slave | DPORT_AHBLITE MPU_TABLE_HINF_REG |
| UDMA1 | DPORT_AHBLITE MPU_TABLE_UHCI1_REG |
| I2S0 | DPORT_AHBLITE MPU_TABLE_I2S0_REG |
| UART1 | DPORT_AHBLITE MPU_TABLE_UART1_REG |
| I2CO | DPORT_AHBLITE MPU_TABLE_I2C_EXTO_REG |
| UDMA0 | Access Forbidden |
| SDIO Slave | DPORT_AHBLITE MPU_TABLE_SLCHOST_REG |
| RMT | DPORT_AHBLITE MPU_TABLE_RMT_REG |
| PCNT | DPORT_AHBLITE MPU_TABLE_PCNT_REG |
| SDIO Slave | DPORT_AHBLITE MPU_TABLE_SLC_REG |
| LED PWM | Access Forbidden |
| Efuse Controller | DPORT_AHBLITE MPU_TABLE_EFUSE_REG |
| Flash Encryption | DPORT_AHBLITE MPU_TABLE_SPI_ENCRYPT_REG |
| PWMO | DPORT_AHBLITE MPU_TABLE_PWM0_REG |
| TIMGO | DPORT_AHBLITE MPU_TABLE_TIMERGROUP_REG |
| TIMG1 | DPORT_AHBLITE MPU_TABLE_TIMERGROUP1_REG |
| SPI2 | Access Forbidden |
| SPI3 | DPORT_AHBLITE MPU_TABLE_SPI2_REG |

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Number and Document Version:**
89 ESP32 TRM (Version 5.6)