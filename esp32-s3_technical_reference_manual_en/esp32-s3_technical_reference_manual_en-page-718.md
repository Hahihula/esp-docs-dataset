**Title:**
Register 15.9. PMS_DMA_APBPERI_SPI3_PMS CONSTRAINT_1_REG (0x0044)

**Body Text:**

- **PMS_DMA_APBPERI_SPI3_PMS CONSTRAINT_SRAM_PMS_0**: Configure SPI3's permission to the instruction region. (R/W)
  
- **PMS_DMA_APBPERI_SPI3_PMS CONSTRAINT_SRAM_PMS_1**: Configure SPI3's permission to the data region 0. (R/W)

- **PMS_DMA_APBPERI_SPI3_PMS CONSTRAINT_SRAM_PMS_2**: Configure SPI3's permission to the data region 1. (R/W)

- **PMS_DMA_APBPERI_SPI3_PMS CONSTRAINT_SRAM_PMS_3**: Configure SPI3's permission to the data region 2. (R/W)

- **PMS_DMA_APBPERI_SPI3_PMS CONSTRAINT_SRAM_CACHEDATAARRAY_PMS_0**: Configure SPI3's permission to SRAM block9. (R/W)

- **PMS_DMA_APBPERI_SPI3_PMS CONSTRAINT_SRAM_CACHEDATAARRAY_PMS_1**: Configure SPI3's permission to SRAM block 10. (R/W)

**Diagram Description:**
The diagram shows a bit map with labels indicating different registers and their corresponding permissions for the instruction region, data regions, and specific SRAM blocks.

- **Bit Labels:** The bits are labeled from `31` down to `0`.
- **Permission Bits:** Each register is associated with one or more permission settings (e.g., `R/W`, `Read Only`).
- **Reset Bit:** There's a bit marked as "Reset" at the end of each group.

**Side Text:**
- On the left side, there are labels indicating different sections such as:
  - "PMS_DMA_APBPERI_SPI3_PMS CONSTRAINT_SRAM_PMS_0"
  - "PMS_DMA_APBPERI_SPI3_PMS CONSTRAINT_SRAM_PMS_1"
  - etc.

**Footer:**
- The footer contains the text “ESP32-S3 TRM (Version 1.7)” and a navigation link labeled “GoBack”.