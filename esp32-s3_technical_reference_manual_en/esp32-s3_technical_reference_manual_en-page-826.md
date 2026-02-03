**Chapter Title:**
Chapter 17 System Registers (SYSTEM)

**Table of System Registers with Descriptions and Reset Values**

| Register Name | Description | System Register |
|----------------|-------------|------------------|
| PWMO           |            | SYSTEM_PWM0_CLK_EN | SYSTEM_PWM0_RST |
| PWM1           |            | SYSTEM_PWM1_CLK_EN | SYSTEM_PWM1_RST |
| LED_PWM Controller |          | SYSTEM_LEDC_CLK_EN | SYSTEM_LEDC_RST |
| ADC Arbiter    |            | SYSTEM_ADC2_ARB_CLK_EN | SYSTEM_ADC2_ARB_RST |
| ADC Controller  |            | SYSTEM_APB_SARADC_CLK_EN | SYSTEM_APB_SARADC_RST |
| Accelerators   |            | SYSTEM_PERIP_CLK_EN1_REG | SYSTEM_PERIP_RST_EN1_REG |
| USB_DEVICE     |            | SYSTEM_USB_DEVICE_CLK_EN | SYSTEM_USB_DEVICE_RST |
| UART2          |            | SYSTEM_UART2_CLK_EN | SYSTEM_UART2_RST |
| LCD_CAM        |            | SYSTEM_LCD_CAM_CLK_EN | SYSTEM_LCD_CAM_RST |
| SDIO_HOST      |            | SYSTEM_SDIO_HOST_CLK_EN | SYSTEM_SDIO_HOST_RST |
| DMA            |            | SYSTEM_DMA_CLK_EN | SYSTEM_DMA_RST |
| HMAC           |            | SYSTEM_CRYPTO_HMAC_CLK_EN | SYSTEM_CRYPTO_HMAC_RST 6 |
| Digital Signature |        | SYSTEM_CRYPTO_DS_CLK_EN | SYSTEM_CRYPTO_DS_RST 7 |
| RSA Accelerator |            | SYSTEM_CRYPTO_RSA_CLK_EN | SYSTEM_CRYPTO_RSA_RST |
| SHA Accelerator |            | SYSTEM_CRYPTO_SHA_CLK_EN | SYSTEM_CRYPTO_SHA_RST |
| AES Accelerator |            | SYSTEM_CRYPTO_AES_CLK_EN | SYSTEM_CRYPTO_AES_RST |
| peri backup     |            | SYSTEM_PERI_BACKUP_CLK_EN | SYSTEM_PERI_BACKUP_RST |

**Note:**
1. Setting the clock enable register to 1 enables the clock, and to 0 disables the clock;
2. Setting the reset enabling register to 1 resets a peripheral, and to 0 disables the reset.
3. Reset registers cannot be cleared by hardware. Therefore, SW reset clear is required after setting the reset registers.
4. UART memory is shared by all UART peripherals, meaning having any active UART peripherals will prevent the UART memory from entering clock-gated state.

5. When DMA is required for peripheral communications, for example, UCHIO, SPI, I2S, LCD_CAM, AES, SHA and ADC, DMA clock should also be enabled.
6. Resetting this bit also resets the SHA accelerator.
7. Resetting this bit also resets the AES, SHA, and RSA accelerators.

**Subsection Title:**
17.3.6 CPU Control Registers

**Description of CPU Control Registers for ESP32-S3**

These registers control CPU0 and CPU1 of ESP32-S3. Note that, by default, only CPU0 is started when the SoC powers up. During this time, the clock of CPU1 is disabled. Therefore, users need to enable CPU1 manually to use both CPU0 and CPU1.

- **SYSTEM_CORE_1 CONTROL_0_REG**
  - Setting the SYSTEM_CONTROL_CORE_1_RESETING bit resets CPU1.
  
- **SYSTEM_CONTROL_CORE_1_CLKGATE_EN**
  - Controls the CPU1 clock.
  
- **SYSTEM_CONTROL_CORE_1_RUNSTALL**
  - When this bit is set, CPU1 will finish the on-going task and stalls.