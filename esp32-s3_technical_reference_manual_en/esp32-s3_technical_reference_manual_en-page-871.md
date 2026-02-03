**Chapter Title:**
Chapter 19 AES Accelerator (AES)

**Section and Register Descriptions with Details:**

- **Register Name:** AES_INC_SEL_REG (0x009C)
  - **Field Description:** 
    - **AES_INC_SEL**: Defines the Standard Incrementing Function for CTR block operation. Set this bit to 0 or 1 to choose INC32 or INC128.
    - **Access Type:** Read/Write
    - **Reset Value:** 0

- **Register Name:** AES_TRIGGER_REG (0x0048)
  - **Field Description:**
    - **AESTrigger**: Set this bit to 1 to start AES operation. Write Only.

- **Register Name:** AES_STATE_REG (0x004C)
  - **Field Description:**
    - **AES State**: Stores the working status of the AES Accelerator.
      - For details, see Table 19.4-1 for Typical AES working mode and Table 19.5-2 for DMA AES working mode.

- **Register Name:** AES_DMA_EXIT_REG (0x00B8)
  - **Field Description:**
    - **AES_DMA_EXIT**: Set this bit to exit AES operation.
      - This register is only effective for DMA-AES operations, Write Only

**Footer Information:**
- Company: Espressif Systems
- Document Version and Type: ESP32-S3 TRM (Version 1.7)
- Page Number: 871
- Links: Submit Documentation Feedback