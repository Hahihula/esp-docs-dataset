**Title: Chapter 12 DPort Registers**

**Subtitle: Register 12.19. DPORT_PERIP_CLK_EN_REG (0xCO)**

**Diagram Description:** 
- A table with a binary representation of the register, labeled from bits 31 to bit 0.

**Body Text and List:**
Set the following bit to enable the clock of the corresponding module. Clear the bit to disable the clock of the corresponding module.
- **DPORT_UART_MEM_CLK_EN**: Shared memory of UART0 ~2. To use any UART peripherals, enable the clock for UART memory. (R/W)
- DPORT_UART2_CLK_EN: UART2 module. (R/W)
- DPORT_SPI_DMA_CLK_EN: SPI_DMA module. (R/W)
- DPORT_I2S1_CLK_EN: I2S1 module. (R/W)
- DPORT_PWM1_CLK_EN: PWM1 module. (R/W)
- DPORT_TWI_CLK_EN: TWAI module. (R/W)
- DPORT_I2C_EXTI_CLK_EN: I2C1 module. (R/W)
- DPORT_PWM0_CLK_EN: PWM0 module. (R/W)
- DPORT_SPI3_CLK_EN: SPI3 module. (R/W)
- DPORT_TIMERGROUP1_CLK_EN: TIMG1 module. (R/W)
- DPORT_EFUSE_CLK_EN: eFuse module. (R/W)
- DPORT_TIMERGROUP_CLK_EN: TIMGO module. (R/W)
- DPORT_UHCI1_CLK_EN: DMA1 module. (R/W)
- DPORT_LEDC_CLK_EN: LEDC module. (R/W)
- DPORT_PCNT_CLK_EN: PCNT module. (R/W)
- DPORT_RMT_CLK_EN: RMT module. (R/W)
- DPORT_UHClO_CLK_EN: UDMA0 module. (R/W)
- DPORT_I2C_EXTO_CLK_EN: I2CO module. (R/W)
- DPORT_SPI2_CLK_EN: SPI2 module. (R/W)

**Footer:** 
Continued on the next page...

**Company Information and Document Version:**
Espressif Systems
ESP32 TRM (Version 5.6)