**Chapter Title:**
Chapter 3 GDMA Controller (GDMA)

**Section Header:**
Register 3.9. GDMA_PD_CONF_REG (0x03C4)

**Body Text with Code Block and Descriptions:**

- **Field Description:** 
  - `GDMA_DMA_RAM_FORCED_PD`
    - Set this bit to force power down GDMA internal memory.
    - Accessible in read/write mode.

- **Field Description:**
  - `GDMA_DMA_RAM_FORCED_PU`
    - Set this bit to force power up GDMA internal memory.
    - Accessible in read/write mode.

- **Field Description:** 
  - `GDMA_DMA_RAM_CLK_F1`
    - Force to open the clock and bypass the gate-clock when accessing the RAM in GDMA; O: A gate-clock will be used when accessing the RAM in GDMA. (R/W)

**Section Header:**
Register 3.10. GDMA_MISC_CONF_REG (0x03C8)

**Body Text with Code Block and Descriptions:**

- **Field Description:** 
  - `GDMA_AHBM_RST_INTER`
    - Set this bit, then clear this bit to reset the internal AHB FSM.
    - Accessible in read/write mode.

- **Field Description:** 
  - `GDMA_AHBM_RST_EXTER`
    - Set this bit, then clear this bit to reset the external AHB FSM.
    - Accessible in read/write mode.

- **Field Description:**
  - `GDMA_ARB_PRI_DIS`
    - Set this bit to disable priority arbitration function. (R/W)

- **Field Description:** 
  - `GDMA_CLK_EN`
    - Force clock on for registers; O: Support clock only when application writes registers.
    - Accessible in read/write mode.

**Footer Information:**
Espressif Systems
381 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback