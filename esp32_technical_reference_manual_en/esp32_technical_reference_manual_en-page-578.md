**Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**Link:**
GoBack

---

**Subtitle:**
Register 26.5. SLCOINT_CLR_REG (0x10)

**Body Text:**

Continued from the previous page...

- **SLCOINT_SLC_FRHOST_BIT3_INT_CLR**: Set this bit to clear `SLCOINT_SLC_FRHOST_BIT3_INT` interrupt.
- **SLCOINT_SLC_FRHOST_BIT2_INT_CLR**: Set this bit to clear `SLCOINT_SLC_FRHOST_BIT2_INT` interrupt.
- **SLCOINT_SLC_FRHOST_BIT1_INT_CLR**: Set this bit to clear `SLCOINT_SLC_FRHOST_BIT1_INT` interrupt.
- **SLCOINT_SLC_FRHOST_BIT0_INT_CLR**: Set this bit to clear `SLCOINT_SLC_FRHOST_BIT0_INT` interrupt.

---

**Subtitle:**
Register 26.6. SLCORX_LINK_REG (0x3C)

**Body Text:**

- **(reserved)**
- **SCLCORX_SLCO_RXLINK_RESTART**: Set this bit to restart and continue the linked list operation for sending packets.
- **SCLCORX_SLCO_RXLINK_START**: Set this bit to start the linked list operation for sending packets. Sending will start from the address indicated by `SLCO_RXLINK_ADDR`.
- **SCLCORX_SLCO_RXLINK_STOP**: Set this bit to stop the linked list operation.

**Bit Description:**
- The lowest 20 bits in the initial address of Slave’s sending linked list.
- (R/W)

---

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)