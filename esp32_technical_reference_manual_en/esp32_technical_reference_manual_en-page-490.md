**Chapter Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**GoBack Link:** GoBack

---

**Section Header:**
Register 24.4. DMARXBASEADDR_REG (0x000C)

**Field Description for START_RECV_LIST:**
START_RECV_LIST This field contains the base address of the first descriptor in the Receive Descriptor list. The LSB Bits[1:0] are ignored and internally taken as all-zero by the DMA. Therefore, these LSB bits are read-only.

**Register Header:**
Register 24.5. DMATXBASEADDR_REG (0x0010)

---

**Section Header:**
STARTTrans_LIST

**Field Description for STARTTrans_LIST:**
This field contains the base address of the first descriptor in the Transmit Descriptor list. The LSB Bits[1:0] are ignored and are internally taken as all-zero by the DMA. Therefore, these LSB bits are read-only.

---

**Section Header:**
Register 24.6. DMASTATUS_REG (0x0014)

**Field Description for EMAC_PMT_INT:**
This bit indicates an interrupt event in the PMT module of the ETH_MAC. The software must read the PMT Control and Status Register in the MAC to get the exact cause of interrupt and clear its source to reset this bit to 1'b0.

---

**Footer Note:** Continued on the next page...

---

**Document Footer:**
Espressif Systems
490 ESP32 TRM (Version 5.6)

**Link for Feedback Submission:**
Submit Documentation Feedback