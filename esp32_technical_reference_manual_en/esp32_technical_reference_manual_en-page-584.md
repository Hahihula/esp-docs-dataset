**Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**Subtitle:**
Register 26.16, SLC0HOST_INT_ST_REG (0x58)

**Diagram Description:**
A diagram showing the layout of a register with various fields labeled as follows:
- (reserved)
- SLCOHOST_SLC0_RX_NEW_PACKET_INT_ST
- ... (continues for each bit position from 31 to 0, including other labels like SLCOHOST_SLC0_TX_OVF_INT_ST)

**Table:**
| Bit Position | Label |
|--------------|-------|
| 31          | (reserved) |
| 26          | SLC0HOST_SLC0_RX_NEW_PACKET_INT_ST |
| ...         | ...   |
| 0           | SLCOHOST_SLC0_TOHOST Bite INT ST |

**Text:**
- "Reset" at the end of each row in the table.
- Each entry describes a masked interrupt status bit for different interrupts related to SDIO operations, such as:
  - SLC0HOST_SLC0_RX_NEW_PACKET_INT
  - SLC0HOST_SLC0_TX_OVF_INT
  - SLCOHOST_SLC0_RX_UDF_INT
  - ... (continues with similar entries)

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Page Number and Document Version:**
584 ESP32 TRM (Version 5.6)