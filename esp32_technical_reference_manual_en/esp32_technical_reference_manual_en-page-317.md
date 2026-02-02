**Chapter Title:**
Chapter 19 UART Controller (UART)

**Body Text:**
UART can also control the software flow by transmitting special characters. Setting UART_SW_FLOW_CON_EN will enable the software flow control function. If the number of data bytes that UART has received exceeds that of the UART_XOFF threshold, the UART controller can send UART_XOFF_CHAR to instruct its counterpart to stop data transmission.

When UART_SW_FLOW_CON_EN is 1, software can send flow control characters at any time. When UART_SEND_XOFF is set, the transmitter will insert a UART_XOFF_CHAR and send it after the current data transmission is completed. When UART_SEND_XON is set, the transmitter will insert a UART_XON_CHAR and send it after the current data transmission is completed.

**Subsection Title:**
19.3.8 UART DMA

**Body Text:**
For information on the UART DMA, please refer to Chapter DMA Controller.

**Subsection Title:**
19.3.9 UART Interrupts

**List of Interrupts with Descriptions:**
- UART_AT_CMD_CHAR_DET_INT: Triggered when the receiver detects the configured at_cmd char.
- UART_RS485_CLASH_INT: Triggered when a collision is detected between transmitter and receiver in RS-485 mode.
- UART_RS485_FRM_ERR_IN: Triggered when a data frame error is detected in RS-485.
- UART_RS485_PARITY_ERR_IN: Triggered when a parity error is detected in RS-485 mode.
- UART_TX_DONE_INT: Triggered when the transmitter has sent out all FIFO data.
- UART_TX_BRK_IDLE DONE_IN: Triggered when the transmitter’s idle state has been kept to a minimum after sending the last data.
- UART_TX_BRK_DONE_IN: Triggered when the transmitter completes sending NULL characters, after all data in transmit-FIFO are sent.
- UART_GLITCH_DET_IN: Triggered when the receiver detects a START bit.
- UART_SW_XOFF_IN: Triggered, if the receiver gets an Xon char when UART_SW_FLOW_CON_EN is set to 1.
- UART_SW_XON_IN: Triggered, if the receiver gets an Xoff char when UART_SW_FLOW_CON_EN is set to 1.
- UART_RXFIFO_TOUT_INT: Triggered when the receiver takes more time than RX_TOUT_THRD to receive a byte.
- UART_BRK_DET_IN: Triggered when the receiver detects a NULL character (i.e. logic O for one NULL character transmission) after stop bits.
- UART_CTS_CHG_IN: Triggered when the receiver detects an edge change of the CTSn signal.
- UART_DSR_CHG_IN: Triggered when the receiver detects an edge change of the DSRn signal.
- UART_RXFIFO_OVF_IN: Triggered when the receiver gets more data than the FIFO can store.
- UART_FRM_ERR_IN: Triggered when the receiver detects a data frame error .
- UART_PARITY_ERR_IN: Triggered when the receiver detects a parity error in the data.

**Footer Text:**
Espressif Systems
317 ESP32 TRM (Version 5.6)
Submit Documentation Feedback