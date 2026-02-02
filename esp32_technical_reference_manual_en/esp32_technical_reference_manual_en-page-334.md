**Chapter Title:**
Chapter 19 UART Controller (UART)

**Register Information:**

- **Register Name:** Register 19.10. UART_CONF1_REG (0x24)
  
  - **Field Descriptions and Values in Hexadecimal:**
    - `UART_RX_TOUT_EN`: This is the enable bit for the UART receive-timeout function.
      - Value: `0x00`
    - `UART_RX_TOUT_THRHD`: This register is used to configure the UART receiver's timeout value when receiving a byte. When using APB_CLK as the clock source, the register counts by UART baud cycle multiplied by 8. When using REF_TICK as the clock source, the register counts by UART baud cycle * 8 / (REF TICK frequency) / (APB_CLK frequency).
      - Value: `0x60`
    - `UART_RX_FLOW_EN`: This is the flow enable bit of the UART receiver; 1: choose software flow control by configuring the sw_sigs signal, 0: disable software flow control.
      - Value: `0x00`
    - `UART_RX_FLOW_THRHD`: When UART_RX_FLOW_EN is 1 and the receiver gets more data than its threshold value, the receiver produces an rtsn_out signal that tells the transmitter to stop transmitting data. The threshold value (rx_flow_thrhd_h3, rx_flow_thrhd).
      - Value: `0x60`
    - `UART_TXFIFO_EMPTY_THRHD`: When the data amount in transmit-FIFO is less than its thresh-old value, it will produce a TXFIFO_EMPTY_INT_RAW interrupt. The threshold value (tx_mem_empty_thrhd, tx fifo empty_thrhd).
      - Value: `0x60`
    - `UART_RXFIFO_FULL_THRHD`: When the receiver gets more data than its threshold value, the receiver will produce an RXFIFO_FULL_INT_RAW interrupt. The threshold value (rx_flow_thrhd_h3, rx fifo full_thrhd).
      - Value: `0x60`

- **Register Name:** Register 19.11. UART_LOWPUSE_REG (0x28)
  
  - **Field Descriptions and Values in Hexadecimal:**
    - `UART_LOWPUSE_MIN_CNT`: This register stores the value of the minimum duration of the low-level pulse. It is used in the baud rate detection process.
      - Value: `0xFFFFF`

**Footer Information:** 
- Page number: 334
- Document version and source information:
  - "ESP32 TRM (Version 5.6)"
  - Company name: Espressif Systems

**Navigation Links/Options:**
- Submit Documentation Feedback