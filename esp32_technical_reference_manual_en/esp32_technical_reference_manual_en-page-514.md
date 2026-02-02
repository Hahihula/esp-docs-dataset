**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Section Header:**
Register 24.26. EMACINTMASK_REG (0x103C)

**Field Description for EMACINTMASK_REG:**
- **LPIINTMASK:** When set, this bit disables the assertion of the interrupt signal because of the setting of the LPI Interrupt Status bit in Register (Interrupt Status Register). (R/W)
- **PMTINTMASK:** When set, this bit disables the assertion of the interrupt signal because of the setting of PMT Interrupt Status bit in Register (Interrupt Status Register). (R/W)

**Field Diagram for EMACINTMASK_REG:**
- The diagram shows a binary representation with bits labeled from 31 to 0. Some bits are marked as "reserved" and others have specific names like LPIINTMASK, PMTINTMASK.

---

**Section Header:**
Register 24.27. EMACADDROHIGH_REG (0x1040)

**Field Description for EMACADDROHIGH_REG:**
- **ADDRESS_ENABLEO:** This bit is always set to 1. (RO)
- **MAC_ADDRESSO_HI:** This field contains the upper 16 bits (47:32) of the first 6-byte MAC address.
  - The MAC uses this field for filtering the received frames and inserting the MAC address in the Transmit Flow Control (Pause) Frames. (R/W)

**Field Diagram for EMACADDROHIGH_REG:**
- Similar to previous diagram, showing binary representation with bits labeled from 31 to 0.

---

**Section Header:**
Register 24.28. EMACADDROLOW_REG (0x1044)

**Field Description for EMACADDROLOW_REG:**
- This field contains the lower 32 bits of the first 6-byte MAC address.
  - This is used by the MAC for filtering the received frames and inserting the MAC address in the Transmit Flow Control (Pause) Frames. (R/W)
  
**Field Diagram for EMACADDROLOW_REG:**
- Similar to previous diagrams, showing binary representation with bits labeled from 31 to 0.

---

**Footer Information:**
Espressif Systems
514 ESP32 TRM (Version 5.6)

**Navigation Links:**
Submit Documentation Feedback

**GoBack Link:** GoBack