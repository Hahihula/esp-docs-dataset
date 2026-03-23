

```markdown
- UHCI_RX_START_INT: Triggered when a separator character has been sent.
```

## 26.5 Programming Procedures

### 26.5.1 Register Type

All UART registers are in APB_CLK domain. According to whether clock domain crossing and synchronization are required, UART registers that can be configured by software are classified into three types, namely immediate registers, synchronous registers, and static registers. Immediate registers are read in APB_CLK domain, and take effect after configured via the APB bus. Synchronous registers are read in Core Clock domain, and take effect after synchronization. Static registers are also read in Core Clock domain, but would not change dynamically. Therefore, for static registers clock domain crossing is not required, and software can turn on and off the clock for the UART transmitter or receiver to ensure that the configuration sampled in Core Clock domain is correct.

#### 26.5.1.1 Synchronous Registers

Read in Core Clock domain, synchronous registers implement the clock domain crossing design to ensure that their values sampled in Core Clock domain are correct. These registers as listed in Table 26.5-1 are configured as follows:

* Enable register synchronization by clearing UART_UPDATE_CTRL to 0;
* Wait for UART_REG_UPDATE to become 0, which indicates the completion of last synchronization;
* Configure synchronous registers;
* Synchronize the configured values to Core Clock domain by writting 1 to UART_REG_UPDATE.

Table 26.5-1. UARTn Synchronous Registers

| Register | Field |
|----------|-------|
| UART_CLKDIV_REG | UART_CLKDIV_FRAG[3:0]<br>UART_CLKDIV[11:0] |
| UART_CONFO_REG | UART_AUTBAUD_EN<br>UART_ERR_WR_MASK<br>UART_TXD_INV<br>UART_RXD_INV<br>UART_IRDA_EN<br>UART_TX_FLOW_EN<br>UART_LOOPBACK<br>UART_IRDA_RX_INV<br>UART_IRDA_TX_EN<br>UART_IRDA_WCTL<br>UART_IRDA_TX_EN<br>UART_IRDA_DPLX<br>UART_STOP_BIT_NUM<br>UART_BIT_NUM |

Cont’d on next page
```