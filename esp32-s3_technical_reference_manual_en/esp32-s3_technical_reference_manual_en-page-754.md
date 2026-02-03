**Title:**
Register 15.44, PMS_CORE_0_IRAMO_PMS_MONITOR_1_REG (0x00E8)

**Diagram Description and Labels:**
- The diagram shows a bit map with labels for each position.
- Bits are labeled from top to bottom as follows:
  - Bit 31 is marked "reserve (read-only)"
  - Bits 2, 1, 0 corresponded respectively
  - Reset

**Bit Definitions:**
1. **PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_CLR**: Set this bit to clear the interrupt triggered when CPU’s IBUS tries to access SRAM or ROM unauthorized.
   - Access type is (R/W)
2. **PMS_CORE_0_IRAMO_PMS_MONITOR_VIOLATE_EN**: Set this bit to enable interrupt when CPU’s IBUS tries to access SRAM or ROM unauthorized.
   - Access type is (R/W)

**Side Text:**
- "Chapter 15 Permission Control (PMS)"
- On the left side, there's a vertical text that reads:
  - Espressif Systems
  - Submit Documentation Feedback

**Footer Information:**
- ESP32-S3 TRM (Version 1.7)