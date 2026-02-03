**Table: Memory Permission Registers**

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| PMS_EDMA_PMS_SPI3_REG | SPI3 External Memory Permission Config Register | 0x02C4 | R/W |
| PMS_EDMA_PMS_UHCIO_LOCK_REG | UHCIO External Memory Permission Lock Register | 0x02C8 | R/W |
| PMS_EDMA_PMS_UHCIO_REG | UHCIO External Memory Permission Config Register | 0x02CC | R/W |
| PMS_EDMA_PMS_I2SO_LOCK_REG | I2S0 External Memory Permission Lock Register | 0x02D0 | R/W |
| PMS_EDMA_PMS_I2SO_REG | I2S0 External Memory Permission Config Register | 0x02D4 | R/W |
| PMS_EDMA_PMS_I2S1_LOCK_REG | I2S1 External Memory Permission Lock Register | 0x02D8 | R/W |
| PMS_EDMA_PMS_I2S1_REG | I2S1 External Memory Permission Config Register | 0x02DC | R/W |
| PMS_EDMA_PMS_LCD_CAM_LOCK_REG | LCD/CAM External Memory Permission Lock Register | 0x02E0 | R/W |
| PMS_EDMA_PMS_LCD_CAM_REG | LCD/CAM External Memory Permission Config Register | 0x02E4 | R/W |
| PMS_EDMA_PMS_AES_LOCK_REG | AES External Memory Permission Lock Register | 0x02E8 | R/W |
| PMS_EDMA_PMS_AES_REG | AES External Memory Permission Config Register | 0x02EC | R/W |
| PMS_EDMA_PMS_SHA_LOCK_REG | SHA External Memory Permission Lock Register | 0x02FO | R/W |
| PMS_EDMA_PMS_SHA_REG | SHA External Memory Permission Config Register | 0x02F4 | R/W |
| PMS_EDMA_PMS_ADC_DAC_LOCK_REG | ADC/DAC External Memory Permission Lock Register | 0x02FC | R/W |
| PMS_EDMA_PMS_ADC_DAC_REG | ADC/DAC External Memory Permission Config Register | 0x0300 | R/W |
| PMS_EDMA_PMS_RMT_LOCK_REG | RMT External Memory Permission Lock Register | 0x0304 | R/W |
| PMS_EDMA_PMS_RMT_REG | RMT Permission Config Register | 0x0308 | R/W |
| **Status Register** | - | - | - |
| PMS_CORE_O_IRAMO_PMS_MONITOR_2_REG | CPUO IBUS Permission Interrupt Register 2 | 0x00EC | RO |
| PMS_CORE_O_DRAMO_PMS_MONITOR_2_REG | CPUO dBUS Permission Interrupt Register 2 | 0x10C | RO |

**Note:** The table lists various memory permission registers and their descriptions, addresses for access in read/write mode (R/W), or Read-Only (RO).