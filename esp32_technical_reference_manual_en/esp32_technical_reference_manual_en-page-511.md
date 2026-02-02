**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Register Information:**
- Register Name: PMT_CSR_REG (0x102C)
- Bit Positions and Values:
  - RWKFILTRST [31, 30] (reserved) 
  - RWKPTR [29, 28] (reserved) 
  - GLBLUCAST [24, 23] to [10, 9]
  - RWKPRCVD [8, 7] and below
  - MGKPKTEN [6, 5] to [0, 0]

**Field Descriptions:**
- **RWKFILTRST:** When this bit is set, it resets the remote RWKPTR register to `3'b000`. (R/WS/SC)
- **RWKPTR:** The maximum value of the pointer is 7. For more details refer to PMT_RWUFFR. (RO)
- **GLBLUCAST:** When set, enables any unicast packet filtered by the MAC (DAFilter) address recognition to be a remote wake-up frame. (R/W)
- **RWKPRCVD:** When set, this bit indicates that power management event is generated because of reception of a remote wake-up frame. This bit will clear on Read into register. (R/SS/RC)
- **MGKPRCVD:** When set, the MAC receiver drops all received frames until it receives expected magic packet or remote wake-up frame. The value must be cleared by MGKPTE, GLBLUCAST, RWKPTR bit is high.
- **RWKPTE:** Enables generation of a power management event because of reception from an up frame (R/W)
- **MGKPKTEN:** When set, enables the MAC receiver to drop all received frames until it receives expected magic packet or remote wake-up frame. This must be cleared by MGKPTE.
- **PWRDWN:** Enables generation a power management event because of reception from an up frame (R/W)

**Footer:**
Espressif Systems
Page 511 ESP32 TRM (Version 5.6)
Submit Documentation Feedback