**Chapter Title:**
Chapter 26 UART Controller (UART)

**Section Titles and Content:**

### 26.5.2.1 Initializing UARTn

- **Body Text:** Initializing UARTn requires two steps: resetting UARTn and enabling register synchronization.
  
- **Subsection - To reset UARTn:**
  - enable the clock for UART RAM by setting SYSTEM_UART_MEM_CLK_EN to 1;
  - enable APB_CLK for UARTn by setting SYSTEM_UARTn_CLK_EN to 1;
  - clear SYSTEM_UARTn_RST;
  - write 1 to UART_RST_CORE;
  - write 1 to SYSTEM_UARTn_RST;
  - clear SYSTEM_UARTn_RST;
  - clear UART_RST CORE.

- **Subsection - To enable register synchronization, clear UART_UPDATE_CTRL.**

### 26.5.2.2 Configuring UARTn Communication

- **Body Text:** To configure UARTn communication:
  - wait for UART_REG_UPDATE to become 0, which indicates the completion of the last synchronization;
  - configure static registers (if any) following Section 26.5.1.2;
  - select the clock source via UART_SCLK_SEL;
  - configure divisor of the divider via UART_SCLK_DIV_NUM, UART_SCLK_DIV_A, and UART_SCLK_DIV_B;
  - configure the baud rate for transmission via UART_CLKDIV and UART_CLKDIV_FRAG;
  - configure data length via UART_BIT_NUM;
  - configure odd or even parity check via UART_PARITY_EN and UART_PARITY;
  - optional steps depending on application ...
  - synchronize the configured values to the Core Clock domain by writing 1 to UART_REG_UPDATE.

### 26.5.2.3 Enabling UARTn

- **Subsection - To enable UARTn transmitter:**
  - configure the TX FIFO’s empty threshold via UART_TXFIFO_EMPTYTHRHD;
  - disable UART_TXFIFO EMPTY_INT interrupt by clearing UART_TXFIFOEMPTYINT_ENA;
  - write data to be sent to UART_RXFIFO_RD_BYTE;
  - clear UART_TXFIFO_EMPTY_INT interrupt by setting UART_TXFIFO_EMPTY_INT_CLR;
  - enable UART_TXFIFO_EMPTY_INT interrupt by setting UART_TXFIFO_EMPTY_INT_ENA;
  - detect UART_TXFIFO_EMPTY_INT and wait for the completion of data transmission.

- **Subsection - To enable UARTn receiver:**
  - configure RXFIFO’s full threshold via UART_RXFIFO_FULLTHRHD;

**Footer Information:** 
Espressif Systems
942 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback