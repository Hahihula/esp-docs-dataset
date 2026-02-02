**Chapter Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**GoBack Link:** GoBack

---

**Section Header:**
Register 26.7 SLCOTX_LINK_REG (0x40)

**Binary Representation Table for Register 26.7 - SLCOTX_LINK_REG (0x40):**

| Bit | Value |
|-----|-------|
| 31-28 | Reserved |
| 27   | SLCO_TXLINK_RESET |
| 26-25 | Reserved |
| 24   | SLCO_TXLINK_START |
| 23-0  | Reserved |

**Description for SLCOTX_SLCO_TXLINK_RESET:**
Set this bit to restart and continue the linked list operation for receiving packets. (R/W)

**Description for SLCOTX_SLCO_TXLINK_START:**
Set this bit to start the linked list operation for receiving packets.
Receiving will start from the address indicated by SLCO_TXLINK_ADDR. (R/W)

**Description for SLCOTX_SLCO_TXLINK_STOP:**
Set this bit to stop the linked list operation for receiving packets.

---

**Section Header:**
Register 26.8 SLCINTVEC_TOHOST_REG (0x4C)

**Binary Representation Table for Register 26.8 - SLCINTVEC_TOHOST_REG (0x4C):**

| Bit | Value |
|-----|-------|
| 31-25 | Reserved |
| 24   | SLCO_TXLINK_ADDR |
| 23-0  | Reserved |

**Description for SLCINTVEC_SLCO_TOHOST_INTVEC:**
The interrupt vector for Slave to interrupt Host. (WO)

---

**Footer Information:** 
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)