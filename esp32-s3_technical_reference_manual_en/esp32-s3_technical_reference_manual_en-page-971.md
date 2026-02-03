**Chapter Title:**
Chapter 26 UART Controller (UART)

**Section Header:**
Register 26.39. UHCI_QUICK_SENT_REG (0x0034)

**Field Descriptions and Values for Register 26.39:**

- **UHCI_SINGLE_SEND_NUM:** This field is used to specify single_send mode.
  - Value representation in binary format:
    ```
    0 0 0 0 0 0 0 0
    ```

- **UHCI_SINGLE_SEND_EN**
  - Description: Set this bit to enable single_send mode to send short packets. (R/W)

- **UHCI_ALWAYS_SEND_NUM**
  - Description: This field is used to specify always_send mode.
  - Value representation in binary format:
    ```
    0x0
    ```

- **UHCI_ALWAYS_SEND_EN**
  - Description: Set this bit to enable always_send mode to send short packets. (R/W)

**Section Header:**
Register 26.40. UHCI_REG_QO_WORDO_REG (0x0038)

**Field Descriptions and Values for Register 26.40:**

- **UHCI_SEND_QO_WORDO**
  - Description: This register is used as a quick_sent register when mode is specified by
    ```
    UHCI_ALWAYS_SEND_NUM or UHCI_SINGLE_SEND_NUM.
    ```

**Section Header:**
Register 26.41. UHCI_REG_QO_WORD1_REG (0x003C)

**Field Descriptions and Values for Register 26.41:**

- **UHCI_SEND_QO_WORD1**
  - Description: This register is used as a quick_sent register when mode is specified by
    ```
    UHCI_ALWAYS_SEND_NUM or UHCI_SINGLE_SEND_NUM.
    ```

**Footer Information:**
Espressif Systems  
971 ESP32-S3 TRM (Version 1.7)  
Submit Documentation Feedback