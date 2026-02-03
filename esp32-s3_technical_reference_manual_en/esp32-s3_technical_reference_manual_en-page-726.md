**Title:**
Register 15.17. PMS_DMA_APBPERI_AES_PMS_CONSTRAIN_1_REG (0x0074)

**Body Text:**

- **PMS_DMA_APBPERI_AES_PMS CONSTRAIN_SRAM_PMS_0**: Configure AES’s permission to the instruction region.(R/W)
  
- **PMS_DMA_APBPERI_AES_PMS CONSTRAIN_SRAM_PMS_1**: Configure AES’s permission to data region0 of SRAM. (R/W)

- **PMS_DMA_APBPERI_AES_PMS CONSTRAIN_SRAM_PMS_2**: Configure AES’s permission to data region1 of SRAM. (R/W)

- **PMS_DMA_APBPERI_AES_PMS CONSTRAIN_SRAM_PMS_3**: Configure AES’s permission to data region2 of SRAM. (R/W)

- **PMS_DMA_APBPERI_AES_PMS CONSTRAIN_SRAM_CACHEDATAARRAY_PMS_0**: Configure AES’s permission to SRAM block9. (R/W)

- **PMS_DMA_APBPERI_AES_PMS CONSTRAIN_SRAM_CACHEDATAARRAY_PMS_1**: Configure AES’s permission to SRAM block10. (R/W)

**Diagram Description:**
The diagram shows a bit map with labels for each register field, indicating the bits that correspond to different permissions and regions.

- **Bit Labels:** 
  - `31` through `0`: These are labeled as `(reserved)` in parentheses.
  
- **Field Values:**
  - The fields from `31` down to `0` have values of `0`, except for the last three bits (`0x3`) which repeat.

**Footer Text (Vertical):**
- "Espressif Systems"
- "Submit Documentation Feedback"

**Page Number and Document Version Information:** 
- Page number: 726
- Document version information at bottom left corner:
  - ESP32-S3 TRM (Version 1.0)

**Navigation Link:**
- GoBack

**Side Texts on the Right Side of Diagram:**
- "Chapter 15 Permission Control (PMS)"

(Note: The text is mirrored and rotated, but I have transcribed it as accurately as possible based on what can be seen in the image.)