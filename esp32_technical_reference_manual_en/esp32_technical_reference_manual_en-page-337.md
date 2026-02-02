**Chapter Title:**
Chapter 19 UART Controller (UART)

**Section Header:**
Register 19.16. UART_SWFC_CONF_REG (0x3C)

**Table Description and Values for Register 19.16:**
- **Field Name:** UART_XOFF_CHAR
  - **Description:** This register stores the Xoff flow control char.
  - **Access Mode:** Read/Write

- **Field Name:** UART_XON_CHAR
  - **Description:** This register stores the Xon flow control char.
  - **Access Mode:** Read/Write

- **Field Name:** UART_XOFF_THRESHOLD
  - **Description:** When the data amount in receive-FIFO is more than what this register indicates, it will send an Xoff char with uart_sw_flow_con_en set to 1. (Read/Write)

- **Field Name:** UART_XON_THRESHOLD
  - **Description:** When the data amount in receive-FIFO is less than what this register indicates, it will send an Xon char with uart_sw_flow_con_en set to 1.
  - **Access Mode:** Read/Write

**Section Header:**
Register 19.17. UART_IDLE_CONF_REG (0x40)

**Table Description and Values for Register 19.17:**
- **Field Name:** UART_TX_BRK_NUM
  - **Description:** This register is used to configure the number of zeros sent after sending data completion.
  - **Access Mode:** Read/Write

- **Field Name:** UART_TX_IDLE_NUM
  - **Description:** This register is used to configure the duration between transfers. (Read/Write)

- **Field Name:** UART_RX_IDLE_THRD
  - **Description:** When the receiver takes more time to receive Byte data than what this register indicates, it will produce a frame-end signal.
  - **Access Mode:** Read/Write

**Footer:**
Espressif Systems  
ESP32 TRM (Version 5.6)