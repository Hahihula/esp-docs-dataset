**Title:**
Chapter 19 UART Controller (UART)

**Body Text:**
being sent. This, in turn, requires that the data rate, STOP bits, parity, etc., be identical at the transmitting and receiving end for the devices to communicate successfully.

A typical UART frame begins with a START bit, followed by a “character” and an optional parity bit for error detection, and it ends with a STO condition. The UART controllers available on the ESP32 provide hardware support for multiple lengths of data and STOP bits. In addition, the controllers support both software and hardware flow control, as well as DMA, for seamless high-speed data transfer. This allows the developer to employ multiple UART ports in the system with minimal software overhead.

**Subtitle:**
19.3.2 UART Architecture

**Image Description (Figure 19.3-1):**
UART Basic Structure
- The image is a block diagram of the UART controller, showing various components such as DMA, UARTn, Rx_FIFO, Tx_FIFO, Rx_FSM, Tx_FSM, and more.

**Body Text:**
Figure 19.3-1 shows the basic block diagram of the UART controller. The UART block can derive its clock from two sources: the 80-MHz APB_CLK, or the reference clock REF_TICK (please refer to Chapter Reset and Clock for more details). These two clock sources can be selected by configuring UART_TICK_REF_ALWAYS_ON.

Then, a divider in the clock path divides the selected clock source to generate clock signals that drive the UART module. UART_CLKDIV_REG contains the clock divider value in two parts — UART_CLKDIV (integral part) and UART_CLKDIV_FRAG (decimal part).

The UART controller can be further broken down into two functional blocks — the transmit block and the receive block.

The transmit block contains a transmit-FIFO buffer, which buffers data awaiting to be transmitted. Software can write Tx_FIFO via APB, and transmit data into Tx_FIFO via DMA. Tx_FIFO_Ctrl is used to control read- and write-access to the Tx_FIFO. When Tx_FIFO is not null, Tx_FSM reads data via Tx_FIFO_Ctrl, and transmits data out according to the set frame format. The outgoing bit stream can be inverted by appropriately configuring the register UART_TXD_INV.

The receive-block contains a receive-FIFO buffer, which buffers incoming data awaiting to be processed. The input bit stream, rxd_in, is fed to the UART controller. Negation of the input stream can be controlled by

**Footer:**
Espressif Systems
312 ESP32 TRM (Version 5.6)
Submit Documentation Feedback