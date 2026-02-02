**Chapter Title:**
Chapter 19 UART Controller (UART)

**Body Text:**

frame is equal to, or larger than, the configured value of register UART_TX_IDLE_NUM, interrupt UART_TX_BRK_IDLE_DONE_INT will be generated.

The receiver can also detect the Break conditions when the RX data line remains logical low for one NULL character transmission, and a UART_BRK_DET_INT interrupt will be triggered to detect that a Break condition has been completed.

The receiver can detect the current bus state through the timeout interrupt UART_RXFIFO_TOUT_INT. The UART_RXFIFO_TOUT_INT interrupt will be triggered when the bus is in the idle state for more than UART_RX_TOUTTHRHD bit time on current baud rate after the receiver has received at least one byte. You can use this interrupt to detect whether all the data from the transmitter has been sent.

**Subsection Title:**
19.3.6 AT_CMD Character Structure

**Diagram Description (Figure 19.3-4):**

Figure caption:
Figure 19.3-4 shows a special AT_CMD character format.
If the receiver constantly receives UART_AT_CMD_CHAR characters and these characters satisfy the following conditions, interrupt UART_AT_CMD_CHAR_DET_INT will be generated.

**Diagram Details:**
- Between the first UART_AT_CMD_CHAR and the last non-UART_AT_CMD_CHAR, there are at least UARTAPER_IDLE_NUM APB clock cycles.
- Between every UART_AT_CMD_CHAR character there must be less than UART_RX_GAP_TOUT APB clock cycles.
- The number of received UART_AT_CMD_CHAR characters must be equal to, or greater than, UART_CHAR_NUM.

**Diagram Details:**
- Between the last UART_AT_CMD_CHAR character received and the next non-UART_AT_CMD_CHAR, there are at least UART_POST_IDLE NUM APB clock cycles.

**Subsection Title:**
19.3.7 Flow Control

**Body Text:**

UART controller supports both hardware and software flow control. Hardware flow control regulates data flow through input signal dsrn_in and output signal rtsn_out. Software flow control regulates data flow by inserting special characters in the flow of sent data and by detecting special characters in the flow of received data.

**Footer Information:**
Espressif Systems
315 ESP32 TRM (Version 5.6)
Submit Documentation Feedback