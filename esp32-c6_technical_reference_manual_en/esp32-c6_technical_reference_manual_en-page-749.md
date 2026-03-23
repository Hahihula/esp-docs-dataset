

```markdown
Figure 27.5-1. UART Programming Procedures

27.5.2.1 Initializing UARTn

To initialize UARTn:

* Write 1 to `PCR_UARTn_RST_EN`.
* Clear `PCR_UARTn_RST_EN`.

27.5.2.2 Configuring UARTn Communication

To configure UARTn communication:

* Wait for `UART_REG_UPDATE` to become 0, which indicates the completion of the last synchronization.
* Select the clock source via `PCR_UARTn_SCLK_SEL`.
* Configure divisor of the divider via `PCR_UARTn_SCLK_DIV_NUM`, `PCR_UARTn_SCLK_DIV_A`, and `PCR_UARTn_SCLK_DIV_B`.
* Configure the baud rate for transmission via `UART_CLKDIV` and `UART_CLKDIV_FRAG`.
* Configure data length via `UART_BIT_NUM`.
* Configure odd or even parity check via `UART_PARITY_EN` and `UART_PARITY`.
* Optional steps depending on application ...
* Synchronize the configured values to the Core Clock domain by writing 1 to `UART_REG_UPDATE`.
```