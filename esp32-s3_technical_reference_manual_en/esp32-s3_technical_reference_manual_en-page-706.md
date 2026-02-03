Title: 
15.9 Register Summary

Body Text:
The addresses of registers starting from PMS in this section are relative to the Permission Control base address, and the addresses of registers starting from APB in this section are relative to the ABP Controller base address. Both base address are provided in Table 4.3-3 in Chapter 4 System and Memory.

Note that all registers with CORE_X in this section apply to both CPUs. The list of registers below is for CPU0 only. CPU1 shares exactly the same set of registers. Adding 0x0400 to the offset of the equivalent of CPU0 register gives you address for CPU1 registers.

For example, the offset for CPU0 register PMS_CORE_0_IRAMO_PMS_MONITOR_O_REG is 0x00E4, the offset for CPU1 equivalent PMS\Core_1_IRAMO_PMS_MONITOR_O_REG should be 0x00E4 + 0x0400, which is 0x04E4.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

Table:
- Name: Configuration Register
- Description (Column): Description of the register.
- Address (Column): The address value associated with each register.
- Access (Column): Indicates whether read/write access is allowed or not, marked as R/W

Table Content:

| PMS_APB_PERIPHERAL_ACCESS_0_REG | APB peripheral configuration register 0 | 0x0008 | R/W |
| PMS_APB_PERIPHERAL_ACCESS_1_REG | APB peripheral configuration register 1 | 0x000C | R/W |
| PMS_INTERNAL_SRAM USAGE_0_REG   | Internal SRAM configuration register 0 | 0x0010 | R/W |
| PMS_INTERNAL_SRAM USAGE_1_REG    | Internal SRAM configuration register 1 | 0x0014 | R/W |
| PMS_INTERNAL_SRAM USAGE_2_REG    | Internal SRAM configuration register 2 | 0x0018 | R/W |
| PMS_DMA_APBPERI_SPI2_PMS CONSTRAIN_0_REG | SPI2 GDMA Permission Config Register O | 0x0038 | R/W |
| PMS_DMA_APBPERI_SPI2_PMS CONSTRAIN_1_REG | SPI2 GDMA Permission Config Register 1 | 0x003C | R/W |
| PMS_DMA_APBPERI_SPI3_PMS CONSTRAIN_0_REG | SPI3 GDMA Permission Config Register O | 0x0040 | R/W |
| PMS_DMA_APBPERI_SPI3_PMS CONSTRAIN_1_REG | SPI3 GDMA Permission Config Register 1 | 0x0044 | R/W |
| PMS_DMA_APBPERI_UHCIO_PMS CONSTRAIN_0_REG | UHCIO GDMA Permission Config Register O | 0x0048 | R/W |
| PMS_DMA_APBPERI_UHCIO_PMS CONSTRAIN_1_REG | UHCIO GDMA Permission Config Register 1 | 0x004C | R/W |
| PMS_DMA_APBPERI_I2S0_PMS CONSTRAIN_0_REG | I2S0 GDMA Permission Config Register O | 0x0050 | R/W |
| PMS_DMA_APBPERI_I2S0_PMS CONSTRAIN_1_REG | I2S0 GDMA Permission Config Register 1 | 0x0054 | R/W |
| PMS_DMA_APBPERI_I2S1_PMS CONSTRAIN_0_REG | I2S1 GDMA Permission Config Register O | 0x0058 | R/W |
| PMS_DMA_APBPERI_I2S1_PMS CONSTRAIN_1_REG | I2S1 GDMA Permission Config Register 1 | 0x005C | R/W |
| PMS_DMA_APBPERI_AES_PMS CONSTRAIN_0_REG | AES GDMA Permission Config Register O | 0x0070 | R/W |
| PMS_DMA_APBPERI_AES_PMS CONSTRAIN_1_REG | AES GDMA Permission Config Register 1 | 0x0074 | R/W |

Footer:
Submit Documentation Feedback
ESP32-S3 TRM (Version 1.7)