**Chapter Title:**
Chapter 9 Interrupt Matrix (INTERRUPT)

**Section Titles and Descriptions with Registers Information:**

1. **Interrupt Core1 Register Details:**
   - **Register Name:** INTERRUPT_CORE1_PERI_BACKUP_INT_MAP_REG  
     **Address:** 0x0984
   - **Register Name:** INTERRUPT_CORE1_DMA_EXTMEM_REJECT_INT_MAP_REG  
     **Address:** 0x0988

2. **Interrupt Source Y Map:**
   - **Register Name:** INTERRUPT_CORE1_SOURCE_Y_MAP
   - **Description:** Map interrupt signal of Source_Y to one of CPU1 external interrupt, can be configured as 0 ~ 5, 8 ~ 10, 12 ~ 14, 17 ~ 28, 30 ~ 31. The remaining values are invalid.
   - **Table Reference:** See table 9-3 for details.

3. **Interrupt Core1 Interrupt Status Register:**
   - **Register Name:** INTERRUPT_CORE1_INTR_STATUS_0_REG
     **Address:** 0x098C

4. **Interrupt Core1 Interrupt Status Register (Continued):**
   - **Register Name:** INTERRUPT_CORE1_INTR_STATUS_1_REG
     **Address:** 0x0990

5. **Interrupt Core1 Interrupt Status for First and Second Sources:**
   - **Register Name:** INTERRUPT_CORE1_INTR_STATUS_0
     **Type:** (RO)
   - **Description:** This register stores the status of the first 32 interrupt sources.
   - **Register Name:** INTERRUPT_CORE1_INTR_STATUS_1
     **Type:** (RO)
   - **Description:** This register stores the status of the second 32 interrupt sources.

**Footer:**
- Page Number: 562
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name and Submission Information:
  - Espressif Systems
  - Submit Documentation Feedback

**Navigation Link:** GoBack