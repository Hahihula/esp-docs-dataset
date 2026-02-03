**Title:**
Register 15.38. PMS_CORE_X_IRAMO_DRAMO_DMA_SPLIT_LINE CONSTRAINT_4_REG (0x00D0)

**Diagram Description:**
- The diagram shows a register layout with various fields labeled as follows:
  - "PMS CORE X DRAMO DMA SRAM LINE O SPLITADDR" repeated multiple times.
  - Each instance of the label is associated with different category numbers from 0 to 6.

**Field Descriptions (from top-left to bottom-right):**
- **Category_0:** PMS_CORE_X_DRAMO_DMA_SRAM_LINE_O_CATEGORY_0
- **Category_1:** PMS_CORE_X_DRAMO_DMA_SRAM_LINE_O_CATEGORY_1
- **Category_2:** PMS_CORE_X_DRAMO_DMA_SRAM_LINE_O_CATEGORY_2
- **Category_3:** PMS_CORE_X_DRAMO_DMA_SRAM_LINE_O_CATEGORY_3
- **Category_4:** PMS_CORE_X_DRAMO_DMA_SRAM_LINE_O_CATEGORY_4
- **Category_5:** PMS_CORE_X_DRAMO_DMA_SRAM_LINE_O_CATEGORY_5
- **Category_6:** PMS_CORE_X_DRAMO_DMA_SRAM_LINE_O_CATEGORY_6

**Field Access Rights:**
- All fields are marked as (R/W), indicating they can be read from and written to.

**Additional Information:**
- The register is described in the context of configuring category field for data internal split line DRAMO_Split_Line_0.
- Each block's configuration corresponds to a specific bit position within the register, with bits 31 through 2 being reserved (not used).

**Footer Note:**
- ESP32-S3 TRM (Version 1.7)