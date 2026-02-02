**Chapter Title:**
Chapter 19 UART Controller (UART)

**Note Section:**
- Note:
  - UART2 doesn’t have any register to reset Tx_FIFO or Rx_FIFO, and the UART1_TXFIFO_RST and UART1_RXFIFO_RST in UART1 may impact the functioning of UART2. Therefore, these 2 registers in UART1 should only be used when the Tx_FIFO and Rx_FIFO in UART2 do not have any data.

**Subsection Title:**
19.3.4 Baud Rate Detection

**Body Text for Subsection:**
- Setting UART_AUTOBAUD_EN for a UART controller will enable the baud rate detection function.
- The Baudrate Detect block shown in Figure 19.3-1 can filter glitches with a pulse width lower than UART_GLITCH_FILTER.

In order to use the baud rate detection feature, some random data should be sent to the receiver before starting the UART communication stream. This is required so that the baud rate can be determined based on the pulse width.
- UART_LOWPUSE_MIN_CNT stores minimum low-pulse width,
- UART_HIGHPULSE_MIN_CNT stores minimum high-pulse width.

By reading these two registers, software can calculate the baud rate of the transmitter.

**Subsection Title:**
19.3.5 UART Data Frame

**Body Text for Subsection:**
Figure 19.3-3 shows the basic data frame structure.
A data frame starts with a START condition and ends with a STOP condition.
The START condition requires 1 bit, and the STOP condition can be realized using 1/1.5/2-bit widths (as set by UART_STOP_BIT_NUM) in RS485 mode turnaround delay may be added by configuring UART_DLO_EN and UART_DL1_EN.

- The START is low level,
- while the STOP is high level.
  
**Figure Description:**
Figure 19.3-3 shows a UART Data Frame Structure with various data bits, parity bit (Parity), stop condition, and break conditions indicated in different states such as START, BIT0 to BIT7, BIT8 to BIT15, Parity, STOP.

The length of the character can comprise from 5 to 8 bits.
When UART_PARITY_EN is set,
the UART controller hardware will add appropriate parity bit after data. 
UART_PARITY is used to select odd parity or even parity if the receiver detects an error in input characters, interrupt UART_PARITY_ERR_INT will be generated.

If the receiver detects errors:
- In the frame format: interrupt UART_FRM_ERR_INT will generate.
- When all data have been transmitted (Interrupt UART_TX_DONE_INT), the transmitter enters Break condition and sends several NULL characters after sending is completed. The number of NULL characters can configure by UART_TX_BRK_NUM, and after the transmitter finishes sending all NULL characters, interrupt UART_TX_BRKDONE_INT generated.

The minimum interval between data frames will be configured with UART_TX_IDLE_NUM.
If idle time for a data frame (BRK) set,
the transmitter enters Break condition. The number of NULL characters can configure by UART_TX_BRK_NUM after the transmitter finishes sending all NULL characters, interrupt UART_TX_BRKDONE_INT generated.

**Footer:**
Espressif Systems
314 ESP32 TRM (Version 5.6)
Submit Documentation Feedback