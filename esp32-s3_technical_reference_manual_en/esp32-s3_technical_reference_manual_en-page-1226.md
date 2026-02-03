**Title:**
Chapter 31 Two-wire Automotive Interface (TWAI®)

**Header:**
Register 31.27. TWAI_INT_ENA_REG (0x0010)

**Menu/Navigation Link:**
GoBack

**Binary Diagram Description:**
The diagram shows a binary representation of the register with various interrupt enable bits labeled as follows:
- TWAI BUS STATE INT ENA
- TWAI ARP LOST INT ENA
- TWAI ERR PASSIVE INT ENA
- (reserved)
- TWAI ERR WARN INT ENA
- TWAI TX INT ENA
- TWAI RX INT ENA

**Interrupt Enable Bits Description:**
1. **TWAI_RX_INT_ENA**: Set this bit to 1 to enable receive interrupt.
2. **TWAI_TX_INT_ENA**: Set this bit to 1 to enable transmit interrupt.
3. **TWAI_ERR_WARN_INT_ENA**: Set this bit to 1 to enable error warning interrupt (R/W).
4. **TWAI_OVERRUN_INT_ENA**: Set this bit to 1 to enable data overrun interrupt (R/W).
5. **TWAI_ERR_PASSIVE_INT_ENA**: Set this bit to 1 to enable error passive interrupt.
6. **TWAI_ARB_LOST_INT_ENA**: Set this bit to 1 to enable arbitration lost interrupt (R/W).
7. **TWAI_BUS_ERR_INT_ENA**: Set this bit to 1 to enable bus error interrupt (R/W).
8. **TWAI BUS STATE INT ENA**: Set this bit to 1 to enable bus state interrupt.

**Footer:**
Espressif Systems
Page number and document version:
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback