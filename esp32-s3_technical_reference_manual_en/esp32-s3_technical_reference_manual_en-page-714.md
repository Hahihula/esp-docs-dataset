**Title:**
Register 15.5. PMS_INTERNAL_SRAM USAGE_2_REG (0x018)

**Diagram Description:**
- The diagram shows a register layout with labels for different fields.
- Fields are labeled as follows:
  - Q^6, Q^7, etc., up to Q^3
  - Reset

**Text Descriptions and Configurations:**

1. **PMS_INTERNAL_SRAM CORE1 TRACE ALLOC**
   - Description: Configure this field to choose a certain block in SRAM as the trace memory block for CPU0.
   - Access Type (R/W)

2. **PMS_INTERNAL_SRAM COREO TRACE USAGE**
   - Description: Configure this field to choose a certain block in SRAM as the trace memory block for CPU1.
   - Access Type (R/W)

3. **PMS_INTERNAL_SRAM COREO TRACE ALLOC**
   - Description: Configure this field to choose a certain 16 KB in the selected trace memory block as trace memory for CPU0.
   - Access Type (R/W)

4. **PMS_INTERNAL_SRAM CORE1 TRACE ALLOC**
   - Description: Configure this field to choose a certain 16 KB in the selected trace memory block as trace memory for CPU1.
   - Access Type (R/W)

**Footer Information:**
- ESP32-S3 TRM (Version 1.7)
- "Submit Documentation Feedback" on left side
- Page number and navigation options ("Go Back") at bottom right corner

**Side Texts:**
- Left Side Vertical Text:
  - Espressif Systems
  
- Right Side Vertical Text:
  - Chapter 15 Permission Control (PMS)