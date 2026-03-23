

```markdown
IrDA protocol  
High-speed data communication using GDMA  
UART as wake-up source  
Software and hardware flow control
```

## 26.3 UART Structure

Figure 26.3-1. UART Architecture Overview

RAM
- UART_MEM_FORCE_PU
- UART_MEM_FORCE_PD
- UART_TX_SIZE
- UART_RX_SIZE
- UART_TXFIFO_RST
- UART_RXFIFO_RST

UART0 Tx_FIFO — apb_wdata → UART0  
UART0 Rx_FIFO ← apb_rdata  

UART1 Tx_FIFO ← apb_wdata → UART1  
UART1 Rx_FIFO ← apb_rdata  

Figure 26.3-2. UART Structure
```markdown
RAM

UART0 Tx_FIFO
UART0 Rx_FIFO

Clock
APB_CLK
RC_FAST_CLK
XTAL_CLK

UART_CLKDIV_REG
UART_CLKSEL

Divider (output to clock source)

UART Core
cts_int ← Hardware Flow Control → ctsn_in  
rts_int ← Software Flow Control → rtsn_out  

Transmitter
apb_wdata → Tx_FIFO (fifo_rd) → Tx_FIFO_Ctrl → Tx_FSM → UART_TXD_INV → txed_out

Receiver
apb_rdata ← Rx_FIFO (fifo_wr) ← Rx_FIFO_Ctrl ← Rx_FSM ← UART_RXD_INV → rxd_in  

Start_Detect  
Baudrate_Detect  
UART_LOOPBACK  

APB_CLK Clock source ↔ APB BUS  

wake_up ← Wakeup_Ctrl
```

Espressif Systems

550

ESP32-C3 TRM (Version 1.3)

Submit Documentation Feedback
```