**Title: Chapter 15 Permission Control (PMS)**

---

### Register Information:

- **Register Name:** PMS_EDMA_PMS_ADC_DAC_REG (0x2FC)
  - **Description:** 
    - `PMS_EDMA_PMS_ADC_DAC ATTR2`  
      Configures ADC Controller’s access to external SRAM Area0. For details, see Table 15.5-4.
    - `PMS_EDMA_PMS_ADC_DAC ATTR1`
      Configures ADC Controller's access to external SRAM Area1. For details, see Table 15.5-4.

---

### Register Information:

- **Register Name:** PMS_EDMA_PMS_RMT_LOCK_REG (0x300)
  - **Description:**
    - `PMS_EDMA_PMS_RMT_LOCK`
      Set this bit to lock the register that configures Remote Control Peripheral’s access to external SRAM.
  
---

**Tables and Diagrams Description:** 

- The image contains two tables, each representing a different set of bits for registers. Each table has columns labeled with binary numbers (0 through 3) indicating positions in the byte or word.

- **First Table:**
  - Bits are arranged horizontally from left to right.
  - Labels on top indicate specific attributes within PMS_EDMA_PMS_ADC_DAC ATTR2 and ATTR1, respectively:
    - `PMS_EDMA_PMS_ADC_DAC ATTR2`
    - `PMS_EDMA_PMS_ADC_DAC ATTR1`

- **Second Table:**
  - Bits are arranged horizontally from left to right.
  - Labels on top indicate specific attributes within PMS_EDMA_PMS_RMT_LOCK:
    - `PMS_EDMA_PMS_RMT_LOCK`

---

**Footer Information:** 

- "ESP32-S3 TRM (Version 1.7)"
- Navigation options: 
  - Left arrow indicating previous page or section.
  - Right arrow labeled "Go Back" for navigation.

---