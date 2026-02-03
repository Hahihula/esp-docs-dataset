**Title:**
Chapter 15 Permission Control (PMS)

**Register Information:**
- **Register Name:** PMS_DMA_APBPERI_PMS_MONITOR_2_REG (0x00B8)
- **Description:** This register is used for monitoring unauthorized DMA access.

**Diagram Description:**
The diagram shows the layout of a 32-bit address with specific bits labeled:
- `PMS_DMA_APBPERI` repeated twice.
- Bits are numbered from right to left, starting at bit '0' and going up to bit '31'.
- The highlighted section indicates that this is an offset register.

**Text Descriptions:**
1. **Field Description:** 
   - PMS_DMA_APBPERI_PMS_MONITOR_VIOLATE_INTR
     - Stores unauthorized DMA access interrupt status.
     - (RO)
2. **Field Description:**
   - PMS_DMA_APBPERI_PMS_MONITOR_STATUS_WORLD
     - Stores the world where the CPU was in when the unauthorized DMA access happened.

**Bit Fields Explanation:** 
- `0b01`: Secure World; 0b10: Non-secure World.
- (RO) Read-only

3. **Field Description:**
   - PMS_DMA_APBPERI_PMS_MONITOR_STATUS_ADDR
     - Stores the address that triggered the unauthorized DMA access.

**Additional Information:** 
- Note on addressing:
  - This is an offset to `0x3c00000` and has a unit of '16', meaning the actual address should be calculated as: `0x3c00000 + PMS_DMA_APBPERI_PMS_MONITOR_VIOLATE_STATUS_ADDR * 16. (RO)`

**Footer Information:** 
- ESP32-S3 TRM (Version 1.7)
- "Submit Documentation Feedback" on the left side.
- Page number: '4' at the bottom center.

This document appears to be a technical reference manual for an integrated circuit, specifically detailing part of its memory management unit related to permission control and monitoring unauthorized DMA access events.