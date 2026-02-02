**Chapter Title:**
Chapter 19 UART Controller (UART)

**GoBack Link:** GoBack

---

**Register Section Header and Descriptions**

- **Register Name**: UHCI_DMA_OUT_EOF_BFR_DESC_ADDR_REG  
  **Address**: 0x44  
  **Description**: This register stores the address of the outlink descriptor when there are some errors in this descriptor. (RO)

- **Register Name**: UHCI_DMA_IN_DSCR_REG  
  **Address**: 0x4C  
  **Description**: The address of the current inlink descriptor x. (RO)

- **Register Name**: UHCI_DMA_IN_DSCR_BFO_REG  
  **Address**: 0x50  
  **Description**: The address of the last inlink descriptor x-1. (RO)

- **Register Name**: UHCI_DMA_IN_DSCR_BF1_REG  
  **Address**: 0x54  
  **Description**: The address of the second-to-last inlink descriptor x-2. (RO)

- **Register Name**: UHCI_DMA_OUT_DSCR_REG  
  **Address**: 0x58  
  **Description**: The address of the current outlink descriptor y.

---

**Footer Information:**
Espressif Systems
351 ESP32 TRM (Version 5.6)
Submit Documentation Feedback