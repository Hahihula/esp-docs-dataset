**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Register Information:**
- **Register Name:** DMANINE_EN_REG (0x001C)
- **Bit Description Table:**

| Bit | Register |
|-----|----------|
| 31  | (reserved) |
| ... | ...      |

**Text Content and Descriptions for Bits in Status Register:**

- **DMAIN_NISE**
  - When this bit is set, normal interrupt summary is enabled. 
  - When this bit is reset, normal interrupt summary is disabled.
  - This bit enables the following interrupts in Status Register (R/W):
    - Bit[0]: Transmit Interrupt.
    - Bit[2]: Transmit Buffer Unavailable.
    - Bit[6]: Receive Interrupt.
    - Bit[14]: Early Receive Interrupt.

- **DMAIN_AISE**
  - When this bit is set, abnormal interrupt summary is enabled. 
  - When this bit is reset, the abnormal interrupt summary is disabled.
  - This bit enables the following interrupts in Status Register (R/W):
    - Bit[1]: Transmit Process Stopped.
    - Bit[3]: Transmit Jabber Timeout.
    - Bit[4]: Receive Overflow.
    - Bit[5]: Transmit Underflow.
    - Bit[7]: Receive Buffer Unavailable.
    - Bit[8]: Receive Process Stopped.
    - Bit[9]: Receive Watchdog Timeout.
    - Bit[10]: Early Transmit Interrupt.
    - Bit[13]: Fatal Bus Error.

- **DMAIN_ERIE**
  - When this bit is set with Normal Interrupt Summary Enable (Bit[16]), the Early Receive Interrupt is enabled. 
  - When this bit is reset, the Early Receive Interrupt is disabled. 

**Footer:**
Continued on the next page...

**Document Footer Information:**
- Page Number: 496
- Document Title: ESP32 TRM (Version 5.6)
- Company Name and Link:
  - Espressif Systems
  - Submit Documentation Feedback