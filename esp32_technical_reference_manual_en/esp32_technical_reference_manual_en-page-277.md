**Chapter Title:**
Chapter 13 Process ID Controller (PID)

**GoBack Link:** GoBack

---

### Register Descriptions:

- **Register 13.6. PIDCTRL_INTERRUPT_ADDR_5_REG (0x014)**
  - Address: `0x040000240`
  - Description: Level 5 interrupt vector entry address.
  - Access Mode: Read/Write
  - Reset Value: Not specified

- **Register 13.7. PIDCTRL_INTERRUPT_ADDR_6_REG (0x018)**
  - Address: `0x04000280`
  - Description: Level 6 interrupt vector entry address.
  - Access Mode: Read/Write
  - Reset Value: Not specified

- **Register 13.8. PIDCTRL_INTERRUPT_ADDR_7_REG (0x01C)**
  - Address: `0x040002CO`
  - Description: NMI interrupt vector entry address.
  - Access Mode: Read/Write
  - Reset Value: Not specified

- **Register 13.9. PIDCTRL_PID_DELAY_REG (0x020)**
  - Address: `0x040002D0`
  - Description:
    - Bit 16 to bit 0 is reserved.
  - Access Mode: Read/Write
  - Reset Value:

- **Register 13.10. PIDCTRL_NMI_DELAY_REG (0x024)**
  - Address: `0x040002E0`
  - Description:
    - Bit 16 to bit 0 is reserved.
  - Access Mode: Read/Write
  - Reset Value:

- **PIDCTRL_PID_DELAY** 
  - Description: Delay until newly assigned PID is valid.

- **PIDCTRL_NMI_DELAY**
  - Description: Delay for disabling CPU NMI interrupt mask signal. 

---

**Footer Information:**  
Espressif Systems  
Page Number: 277  
Document Version: ESP32 TRM (Version 5.6)  

**Feedback Link:** Submit Documentation Feedback