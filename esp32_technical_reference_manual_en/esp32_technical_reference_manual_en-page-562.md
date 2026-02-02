**Title:**
Chapter 25 Two-Wire Automotive Interface (TWAI)

**Header:**
Register 25.27. TWAI_INT_ENA_REG (0x0010)

**Binary Diagram Description:**
- The diagram shows a binary representation of the register with various bits labeled.
- Bits are numbered from left to right, starting at bit '31' on the far left and ending at bit '0' towards the center-right.

**Bit Labels in Binary Representation (from top-left):**
- TWAI BUS ERR INT ENA
- TWAI_ARB LOST INT ENA
- TWAI_ERR WARN PASSIVE INT ENA
- TWAI_RX INT ENA
- TWAI_TX INT ENA
- TWAI_ERR WARN INT ENA
- TWAI_ERR PASSIVE INT ENA
- TWAI_RX INT ENA

**Text Descriptions:**
1. **TWAI_RX_INT_ENA**: Set this bit to 1 to enable receive interrupt.
2. **TWAI_TX_INT_ENA**: Set this bit to 1 to enable transmit interrupt.
3. **TWAI_ERR_WARN_INT_ENA**: Set this bit to 1 to enable error warning interrupt (R/W).
4. **TWAI_OVERRUN_INT_ENA**: Set this bit to 1 to enable data overrun interrupt (R/W).
5. **TWAI_ERR_PASSIVE_INT_ENA**: Set this bit to 1 to enable error passive interrupt.
6. **TWAI_ARB_LOST_INT_ENA**: Set this bit to 1 to enable arbitration lost interrupt (R/W).
7. **TWAI_BUS_ERR_INT_ENA**: Set this bit to 1 to enable error interrupt.

**Footer:**
- Page number and document version information:
  - "Espressif Systems"
  - "562 ESP32 TRM (Version 5.6)"
  - Links for submitting documentation feedback are provided at the bottom of each page, but they aren't clickable in this format.
  
**Navigation Link:**
- A link labeled "GoBack" is present to navigate back from where it was accessed.

This document appears to be a technical reference manual section detailing specific interrupt enable settings within an automotive interface register for TWAI (Two-Wire Automotive Interface).