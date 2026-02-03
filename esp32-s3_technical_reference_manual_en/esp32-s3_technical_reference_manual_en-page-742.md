**Title:**
Register 15.33. PMS_DMA_APBPERI_PMS_MONITOR_3_REG (0x0DBC)

**Body Text:**

- **PMS_DMA_APBPERI_PMS_MONITOR_VIOLATE_STATUS_WR**: Store the direction of unauthorized GDMA access.
  - `1`: write
  - `0`: read

- **PMS_DMA_APBPERI_PMS_MONITOR_VIOLATE_STATUS_BYTEEN**: Stores the byte information of unauthorized GDMA access.

**Diagram Description:**
The diagram shows a bitfield layout for Register 15.33, with specific bits labeled:
- Bits [31] to [0]: Reserved
- Bit [16]: PMS_DMA_APBPERI_PMS_MONITOR_VIOLATE_STATUS_WR (bit position and meaning as described above)
- Bit [15]: PMS_DMA_APBPERI_PMS_MONITOR_VIOLATE_STATUS_BYTEEN (bit position and meaning as described above)

**Footer:**
ESP32-S3 TRM (Version 1.7)