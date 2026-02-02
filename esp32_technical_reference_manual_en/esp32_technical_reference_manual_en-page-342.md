**Title: Chapter 19 UART Controller (UART)**

**Register Information**
- **Register Name:** Register 19.28. UART_NEGPULSE_REG (0x6c)
- **Bit Description:** 
  - Bits [31, 20]: Reserved.
  - Bits [19, 0]: UART_NEGEDGE_MIN_CNT
    - This register stores the count of RxD negative edges. It is used in the autobaud detection process.

**Section: 19.5.2 UHCI Registers**
- **Description:** The addresses in this section are relative to the UDMA base address provided in Table 3.3-6 in Chapter 3 System and Memory.
- Note on absolute register addresses:
  - Refer to Section [19.4.2 UHCI Register Summary](#).
  
**Note for Reserved Fields:**
- For how to program reserved fields, refer to Section Programming Reserved Register Field.

**Register Information (Continued)**
- **Register Name:** Register 19.29. UHCI_CONF0_REG (0x0)
- **Bit Description with Values and Access Rights:**
  - Bits [31, 22]: Reserved.
  - Bits [21, 20]: Reserved.
  - Bits [18, 17]: Reserved.
  - Bits [16, 15]: Reserved.
  - Bits [14, 9]: Reserved.
  - Bits [8, 3]: Reserved.
  - Bits [2, 0]: Reserved.

**Bit Fields:**
- **UHCI_ENCODE_CRC_EN:** Reserved. Please initialize it to O. (R/W)
- **UHCI_LEN_EOF_EN:** Reserved. Please initialize it to O. (R/W)
- **UHCI_UART_IDLE_EOF_EN:** Reserved. Please initialize it to 0. (R/W)
- **UHCI_CRC_REC_EN:** Reserved. Please initialize it to 0. (R/W)
- **UHCI_HEAD_EN:** Reserved. Please initialize it to 0. (R/W)
- **UHCI_SEPER_EN:** Set this bit to use a special char and separate the data frame. (R/W)
- **UHCI_UART2_CE:** Set this bit to use UART2 and transmit or receive data. (R/W)
- **UHCI_UART1_CE:** Set this bit to use UART1 and transmit or receive data. (R/W)
- **UHCI_UART0_CE:** Set this bit to use UART and transmit or receive data. (R/W)

**Footer:**
- Espressif Systems
- Page number 342
- Document version ESP32 TRM (Version 5.6)