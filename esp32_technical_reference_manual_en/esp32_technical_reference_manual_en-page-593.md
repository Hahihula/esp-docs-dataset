**Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**Subtitle:**
Register 26.32. SLCOHOST_INT_CLR_REG (0xD4)

**Diagram Description:**
A diagram showing the layout of a register with various fields labeled, such as "SLCOHOST_SLC0_RX_NEW_PACKET_INTEGR", etc., each followed by a bit number and some are marked as "(reserved)". The bits range from 31 to 0.

**Table:**

| Field Name | Description |
|------------|-------------|
| SLCOHOST_SLC0_RX_NEW_PACKET_INTEGR | Set this bit to clear the SLCOHOST_SLC0_RX_NEW_PACKET_INTEGR interrupt. (WO) |
| SLCOHOST_SLC0_TX_OVF_INTEGR | Set this bit to clear the SLCOHOST_SLC0_TX_OVF_INT_interrupt. (WO) |
| SLCOHOST_SLC0_RX_UDF_INTEGR | Set this bit to clear the SLCOHOST_SLC0_RX_UDF_INT_interrupt. (WO) |
| ... | ... |

**Additional Information:**
- Each entry in the table has a corresponding description indicating what action should be taken with that specific field.
- The fields are related to interrupt clearing for different operations of an SDIO slave controller.

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Page Number and Document Version:**
593 ESP32 TRM (Version 5.6)