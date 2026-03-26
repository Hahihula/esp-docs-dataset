

```markdown
Chapter 42 UART Controller (UART) GoBack

## 42.5.2 Detailed Steps

Figure 42.5-1 illustrates the process to program UART controllers, namely initialize UART, configure registers, enable the UART transmitter or receiver, and finish data transmission.

![Figure 42.5-1. UART Programming Procedures](image)

### 42.5.2.1 Initializing UARTn

To initialize UARTn:

* Write 1 to `HP_SYS_CLKRST_RST_EN_UARTn_APB`.
* Clear `HP_SYS_CLKRST_RST_EN_UARTn_APB` to 0.
* Write 1 to `HP_SYS_CLKRST_RST_EN_UARTn_CORE`.
* Clear `HP_SYS_CLKRST_RST_EN_UARTn_CORE` to 0.

### 42.5.2.2 Configuring UARTn Communication

To configure UARTn communication:

* Wait for `UART_REG_UPDATE` to become 0, which indicates the completion of the last synchronization.
* Select the clock source via `HP_SYS_CLKRST_UARTn_CLK_SRC_SEL`.
* Configure divisor of the divider via `HP_SYS_CLKRST_UARTn_SCLK_DIV_NUM`, `HP_SYS_CLKRST_UARTn_SCLK_DIV_DENOMINATOR`, and
```