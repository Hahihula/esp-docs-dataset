

```markdown
Chapter 26 UART Controller (UART)

GoBack

26.5.2.1 Initializing UARTn

To initialize UARTn:

- enable the clock for UART RAM by setting SYSTEM_UART_MEM_CLK_EN to 1;
- enable APB_CLK for UARTn by setting SYSTEM_UARTn_CLK_EN to 1;
- clear SYSTEM_UARTn_RST;
- write 1 to UART_RST_CORE;
- write 1 to SYSTEM_UARTn_RST;
- clear SYSTEM_UARTn_RST;
- clear UART_RST_CORE;
- enable register synchronization by clearing UART_UPDATE_CTRL.

26.5.2.2 Configuring UARTn Communication

To configure UARTn communication:

- wait for UART_REG_UPDATE to become 0, which indicates the completion of the last synchronization;
- configure static registers (if any) following Section 26.5.1.2;
- select the clock source via UART_SCLK_SEL;
- configure divisor of the divider via UART_SCLK_DIV_NUM, UART_SCLK_DIV_A, and UART_SCLK_DIV_B;
- configure the baud rate for transmission via UART_CLKDIV and UART_CLKDIV_FRAG;
- configure data length via UART_BIT_NUM;
- configure odd or even parity check via UART_PARITY_EN and UART_PARITY;
- optional steps depending on application ...
- synchronize the configured values to the Core Clock domain by writing 1 to UART_REG_UPDATE.

26.5.2.3 Enabling UARTn

To enable UARTn transmitter:

- configure TX FIFO's empty threshold via UART_TXFIFO_EMPTY_THRDH;
- disable UART_TXFIFO_EMPTY_INT interrupt by clearing UART_TXFIFO_EMPTY_INT_ENA;
- write data to be sent to UART_RXFIFO_RD_BYTE;
- clear UART_TXFIFO_EMPTY_INT interrupt by setting UART_TXFIFO_EMPTY_INT_CLR;
- enable UART_TXFIFO_EMPTY_INT interrupt by setting UART_TXFIFO_EMPTY_INT_ENA;
- detect UART_TXFIFO_EMPTY_INT and wait for the completion of data transmission.

To enable UARTn receiver:

- configure RX FIFO's full threshold via UART_RXFIFO_FULL_THRDH;
- enable UART_RXFIFO_FULL_INT interrupt by setting UART_RXFIFO_FULL_INT_ENA;

Espressif Systems
566
ESP32-C3 TRM (Version 1.3)
Submit Documentation Feedback
```