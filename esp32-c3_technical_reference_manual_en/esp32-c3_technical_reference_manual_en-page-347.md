

```markdown
Register 14.13. PMS_DMA_APBPERI_I2SO_PMS_CONSTRAIN_1_REG (0x004C)

| Bit 31 | Bit 30 | ... | Bit 8 | Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 |
|--------|--------|-----|-------|-------|-------|-------|-------|-------|-------|-------|-------|
|        |        | ... | (reserved) | PMS_DMA_APBPERI_I2SO_PMS_CONSTRAIN_SRAM_M_MODE_PMS_3 | PMS_DMA_APBPERI_I2SO_PMS_CONSTRAIN_SRAM_M_MODE_PMS_2 | PMS_DMA_APBPERI_I2SO_PMS_CONSTRAIN_SRAM_M_MODE_PMS_1 | PMS_DMA_APBPERI_I2SO_PMS_CONSTRAIN_SRAM_M_MODE_PMS_0 | Reset |
|        |        | ... |           | 0x3   | 0x3   | 0x3   | 0x3   |       |       |       |       |

PMS_DMA_APBPERI_I2SO_PMS_CONSTRAIN_SRAM_M_MODE_PMS_0 Configure I2S's permission to the instruction region. (R/WL)  
PMS_DMA_APBPERI_I2SO_PMS_CONSTRAIN_SRAM_M_MODE_PMS_1 Configure I2S's permission to the data regionO of SRAM. (R/WL)  
PMS_DMA_APBPERI_I2SO_PMS_CONSTRAIN_SRAM_M_MODE_PMS_2 Configure I2S's permission to the data region1 of SRAM. (R/WL)  
PMS_DMA_APBPERI_I2SO_PMS_CONSTRAIN_SRAM_M_MODE_PMS_3 Configure I2S's permission to the data region2 of SRAM. (R/WL)
```