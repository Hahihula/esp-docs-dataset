**Title:**
Register 15.21. PMS_DMA_APBPERI_ADC_DAC_PMS CONSTRAINT_1_REG (0x0084)

**Body Text with Descriptions of Register Bits and Permissions:**

- **PMS_DMA_APBPERI_ADC_DAC_PMS CONSTRAINT_SRAM_PMS_0**: Configure ADC_DAC’s permission to the instruction region. (R/W)
  
- **PMS_DMA_APBPERI_ADC_DAC_PMS CONSTRAINT_SRAM_PMS_1**: Configure ADC_DAC’s permission to data region 0 of SRAM. (R/W)

- **PMS_DMA_APBPERI_ADC_DAC_PMS CONSTRAINT_SRAM_PMS_2**: Configure ADC_DAC’s permission to data region 1 of SRAM. (R/W)

- **PMS_DMA_APBPERI_ADC_DAC_PMS CONSTRAINT_SRAM_PMS_3**: Configure ADC_DAC’s permission to data region 2 of SRAM. (R/W)

- **PMS_DMA_APBPERI_ADC_DAC_PMS CONSTRAINT_SRAM_CACHEDATAARRAY_PMS_0**: Configure ADC_DAC’s permission to SRAM block 9. (R/W)

- **PMS_DMA_APBPERI_ADC_DAC_PMS CONSTRAINT_SRAM_CACHEDATAARRAY_PMS_1**: Configure ADC_DAC’s permission to SRAM block 10. (R/W)

**Diagram Description:**
The diagram shows a bit map with labels indicating the register bits and their corresponding permissions for different regions of SRAM.

- **Bit Labels:** The top row lists various registers related to PMS_DMA_APBPERI_ADC_DAC_PMS CONSTRAINT_1_REG.
  
- **Permission Bits (0x3):** Each column under "reserved" shows a bit pattern with all 0s except the last three bits, which are labeled as '0x3', indicating that these specific bits grant read/write permission.

The diagram visually represents how different permissions for ADC_DAC to various SRAM regions and blocks can be configured using specific register settings.