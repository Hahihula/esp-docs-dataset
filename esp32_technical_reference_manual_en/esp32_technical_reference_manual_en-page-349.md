**Chapter Title:**
Chapter 19 UART Controller (UART)

**GoBack Link:** [GoBack](#)

---

**Register Section Header:**

- **Register Name and Address:**
  - Register 19.37, UHCI_DMA_OUT_LINK_REG (0x24)
  
- **Description of the Register:**
  - `UHCI_OUTLINK PARK`: The outlink descriptor’s FSM is in idle state; O: the outlink descriptor’s FSM is working.
    - Access Type: Read/Write
    - Value Range: 1

- **Bit Description and Functionality for UHCI_OUTLINK PARK:**
  - Bit 30 to bit 27 (reserved)
  - Bit 29, 28:
    - `UHCI_OUTLINK_RESET`: Set this bit to restart the outlink descriptor from the last address.
      - Access Type: Read/Write
      - Value Range: Not specified

- **Bit Description and Functionality for UHCI_OUTLINK START:**
  - Bit 30, 29:
    - `UHCI_OUTLINK START`: Set this bit to start a new outlink descriptor.

- **Bit Description and Functionality for UHCI_OUTLINK STOP:**
  - Bit 31:

- **Bit Description and Functionality for UHCI_OUTLINK ADDR:**
  - This register stores the least significant 20 bits of the first outlink descriptor’s address.
    - Access Type: Read/Write
    - Value Range: Not specified

---

**Register Section Header:**

- **Register Name and Address:**
  - Register 19.38, UHCI_DMA_IN_LINK_REG (0x28)

- **Description of the Register:**
  - `UHCI_INLINK PARK`: The inlink descriptor’s FSM is in idle state; O: the inlink descriptor’s FSM is working.
    - Access Type: Read/Write
    - Value Range: Not specified

- **Bit Description and Functionality for UHCI_INLINK PARK:**

- **Bit Description and Functionality for UHCI_INLINK START:**
  - Bit 30, 29:
    - `UHCI_INLINK START`: Set this bit to start dealing with the inlink descriptors.

- **Bit Description and Functionality for UHCI_INLINK STOP:**
  - This register stores the least significant bits of the first inlink descriptor’s address.
    - Access Type: Read/Write
    - Value Range: Not specified

---

**Footer Information:**  
Espressif Systems  
349  
ESP32 TRM (Version 5.6)  

**Feedback Link:** [Submit Documentation Feedback](#)