**Title: Chapter 19 UART Controller (UART)**

---

### Register Section:

- **Register Name:** UHCI_CONF1_REG (0x2C)
  - **Fields Description:**
    - `UHCI_TX_ACK_NUM_RE`: Reserved. Please initialize to O. (R/W)
    - `UHCI_TX_CHECK_SUM_RE`: Reserved. Please initialize to O. (R/W)
    - `UHCI_CHECK_SEQ_EN`: Reserved. Please initialize to O. (R/W)
    - `UHCI_CHECK_SUM_EN`: Reserved. Please initialize to O. (R/W)

- **Register Name:** UHCI_DMA_OUT_EOF_DES_ADDR_REG (0x38)
  - Description: This register stores the address of the outlink descriptor when the EOF bit in this descriptor is 1. (RO)

- **Register Name:** UHCI_DMA_IN_SUC_EOF_DES_ADDR_REG (0x3C)
  - Description: This register stores the address of the inlink descriptor when the EOF bit in this descriptor is 1. (RO)

- **Register Name:** UHCI_DMA_IN_ERR_EOF_DES_ADDR_REG (0x40)
  - Description: This register stores the address of the inlink descriptor when there are some errors in this descriptor. (RO)

---

**Footer Information:**
- Page Number: 350
- Document Title: ESP32 TRM (Version 5.6)
- Company Name: Espressif Systems

**Action Links:** 
- Submit Documentation Feedback