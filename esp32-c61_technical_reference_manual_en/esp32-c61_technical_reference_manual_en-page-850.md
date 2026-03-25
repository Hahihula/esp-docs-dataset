

```markdown
Chapter 25 UART Controller (UART) GoBack

25.6.2 Detailed Steps

Figure 25.6-1 illustrates the process to program UART controllers, namely initialize UART, configure registers, enable the UART transmitter or receiver, and finish data transmission.

![Flowchart: Start → Initial → UART transfer configuration → Set UART_REG_UPDATE=1 → Decision (UART_REG_UPDATE == 0?) → If N loop back to "Registers configuration flow" → If Y proceed to "Start UART TX/RX Flow" → End]

Figure 25.6-1. UART Programming Procedures

25.6.2.1 Initializing UARTn

To initialize UARTn:

* Write 1 to HP_SYS_CLKRST_RST_EN_UARTn_APB.
* Clear HP_SYS_CLKRST_RST_EN_UARTn_APB to 0.
* Write 1 to HP_SYS_CLKRST_RST_EN_UARTn_CORE.
* Clear HP_SYS_CLKRST_RST_EN_UARTn_CORE to 0.

25.6.2.2 Configuring UARTn Communication

To configure UARTn communication:

* Wait for UART_REG_UPDATE to become 0, which indicates the completion of the last synchronization.
* Select the clock source via HP_SYS_CLKRST_UARTn_CLK_SRC_SEL.
* Configure divisor of the divider via HP_SYS_CLKRST_UARTn_SCLK_DIV_NUM, HP_SYS_CLKRST_UARTn_SCLK_DIV_DENOMINATOR, and
```