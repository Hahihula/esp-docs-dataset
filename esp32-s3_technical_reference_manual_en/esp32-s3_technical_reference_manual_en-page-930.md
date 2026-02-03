**Title:**
Chapter 26 UART Controller (UART)

**GoBack**

**Body Text with Code and Formulas:**
- **Formula:** `B_UART = f_clk / (UARTPOSEDGE_MIN_CNT + 1) / 2`
- **Formula:** `B_UART = f_clk / (UARTEGEDGE_MIN_CNT + 1) / 2`

3. If UART signals are weak along rising edges, use `UARTNEGEDGE_MIN_CNT` to determine the transmitter’s baud rate as follows:

**Subtitle:**
26.4.4 UART Data Frame

**Diagram Description with Labels and Annotations (Figure 26.4-4):**
- Diagram of a UART data frame structure.
- Labeled parts include START, BIT0, BIT1, BITn, Parity, STOP, next, data0, data1, data2,..., datan, brk_num, UART_TX_IDLE_NUM.

**Caption for Figure:**
Figure 26.4-4 Structure of UART Data Frame

**Body Text with Explanation and Details (Section 26.4.6):**
- The actual data length can be anywhere between 5 ~ 8 bits.
- When `UART_PARITY_EN` is set, a parity bit added after data bits are included in the frame configuration.

**Additional Information:**
- UART_BIT_NUM
- UART_TX_IDLE_NUM

**Explanation of Interrupts and Conditions (Section on UART Framing):**
- If all data have been sent to Tx_FIFO or Rx_FIFO:
  - `UART_TX DONE_INT` interrupt is generated.
  - `UART_TX BRK` interrupt when the transmitter enters Break condition by sending several NULL characters in which the TX data line goes low.

**Additional Interrupts:**
- `UART_TX_BRK_DET_INT`: Triggered to detect a Break completion after receiving one character transmission and RX data line remains logical high for more than one byte.
- `UART_RX_FIFO_TOUT_INT`: Trigger when bus is idle state or Rx FIFO timeout occurs, indicating the end of data reception.

**Footer:**
Espressif Systems
930 ESP32-S3 TRM (Version 1.7)