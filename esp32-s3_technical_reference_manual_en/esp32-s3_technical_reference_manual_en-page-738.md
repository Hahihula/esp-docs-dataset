**Title:**
Register 15.29. PMS_DMA_APBPERI_SDIO_PMS CONSTRAINT_1_REG (0x00AC)

**Table Description:**
- The table is a bitfield layout for the register.
- Bit positions are labeled from left to right as follows:
  - Bits [31] through [0]
- Each column represents different bits with specific functions, indicated by labels such as "PMS_DMA_APBPERI_SDIO_PMS_CONSTRAINT_SRAM_PMS_0" and others.

**Bitfield Labels:**
- PMS_DMA_APBPERI_SDIO_PMS CONSTRAINT_SRAM_PMS_0
- PMS_DMA_APBPERI_SDIO_PMS CONSTRAINT_SRAM_PMS_1
- PMS_DMA_APBPERI_SDIO_PMS CONSTRAINT_SRAM_PMS_2
- PMS_DMA_APBPERI_SDIO_PMS CONSTRAINT_SRAM_PMS_3

**Descriptions:**
- **PMS_DMA_APBPERI_SDIO_PMS CONSTRAINT_SRAM_PMS_0:** Configure SDIO's permission to the instruction region. (R/W)
- **PMS_DMA_APBPERI_SDIO_PMS CONSTRAINT_SRAM_PMS_1:** Configure SDIO's permission to data region 0 of SRAM. (R/W)
- **PMS_DMA_APBPERI_SDIO_PMS CONSTRAINT_SRAM_PMS_2:** Configure SDIO's permission to data region 1 of SRAM. (R/W)
- **PMS_DMA_APBPERI_SDIO_PMS CONSTRAINT_SRAM_PMS_3:** Configure SDIO's permission to data region 2 of SRAM. (R/W)

**Additional Descriptions:**
- PMS_DMA_APBPERI_SDIO_PMS CONSTRAINT_SRAM_CACHEDATAARRAY_PMS_0
- PMS_DMA_APBPERI_SDIO_PMS CONSTRAINT_SRAM_CACHEDATAARRAY_PMS_1

These bits configure SDIO's permissions to different regions of SRAM and cachedataarray, with read/write access specified.