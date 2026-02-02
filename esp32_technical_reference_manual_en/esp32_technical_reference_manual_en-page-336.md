**Title:**
Chapter 19 UART Controller (UART)

**Subtitles and Sections with Descriptions of Registers:**

- **Register 19.14. UART_FLOW_CONFIG_REG (0x34)**
  - **Field Descriptions in Binary Format:** 
    ```
    6   5   4   3   2   1   0
    |----|----|----|----|----|----|----|
    UART_SEND_XOFF | UART_SEND_XON | ... | ...
    UART_FORCE_XOFF | ... | ... | ...
    UART FORCE XON | ... | ... | ...
    UART_XONOFF_DEL | ... | ... | ...
    UART_SW_FLOW_CONFIG_EN
    ```
  - **Field Descriptions:**
    - `UART_SEND_XOFF`: Hardware auto-clear; set to 1 to send Xoff char. (R/W)
    - `UART_SEND_XON`: Hardware auto-clear; set to 1 to send Xon char. (R/W)
    - `UART_FORCE_XOFF`: Set this bit to stop the internal CTSn and stop the transmitter from sending data.
    - `UART FORCE XON`: Set this bit to clear the internal CTSn and enable the transmitter to continue sending data.
    - `UART_XONOFF_DEL`: Set this bit to remove the flow-control char from the received data. (R/W)
    - `UART_SW_FLOW_CONFIG_EN`: Set this bit to enable software flow control. It is used with register sw_xon or sw_xoff.

- **Register 19.15. UART_SLEEP_CONFIG_REG (0x38)**
  - **Field Description in Binary Format:**
    ```
    10   9   8   ...   ...
    |----|----|----|
    |----|----|
    UART_ACTIVE_THRESHOLD
    ```
  - **Field Description:**
    - `UART ACTIVE THRESHOLD`: When the number of positive edges of Rx signal is larger than or equal to (UART_ACTIVE_THRESHOLD+2), the system emerges from Light-sleep mode and becomes active. (R/W)

**Footer Information:**
- Page Number: "336"
- Document Title: ESP32 TRM (Version 5.6)
- Company Name: Espressif Systems
- Link Texts:
  - Submit Documentation Feedback

**Navigation Links:**
- GoBack