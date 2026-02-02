**Title: Chapter 19 UART Controller (UART)**

---

### Register 19.23. UART_MEM_CONF_REG (0x58)

| Field | Offset |
|-------|--------|
| (reserved) | - |
| UART_TX_MEM_EMPTY_THRHD | 31-24 |
| UART_RX_MEM_FULL_THRESHOLD_H2 | 27-24 |
| UART_XON_XOUT_THRESHOLD_H2 | 20-18 |
| UART_RX_FLOW_THRESHOLD_H3 | 17-15 |
| (reserved) | - |
| UART_TX_SIZE | 14-11 |
| UART_MEM_PD | 10-6 |
| UART_RX_SIZE | 5-2 |
| UART_TXSize | 1 |

**Description:**

- **UART_TX_MEM_EMPTY_THRHD**: Refer to the description of `TXFIFO_EMPTY THRHD`. (R/W)
- **UART_RX_MEM_FULL_THRESHOLD_H2**: Refer to the description of `RXFIFO_FULL THRHD`. (R/W)
- **UART_XOFF_THRESHOLD_H2**: Refer to the description of `UART_XOFF THRHD`. (R/W)
- **UART_XON_THRESHOLD_H2**: Refer to the description of `UART_XON THRHD`. (R/W)
- **UART_RX_TOUTTHRHD_H3**: Refer to the description of `RX_TOUTTHRHD`. (R/W)
- **UART_RX_FLOWTHRHD_H3**: Refer to the description of `RX_FLOWTHRHD`. (R/W)

**Additional Registers:**

- **UART_TX_SIZE**: This register is used to configure the amount of memory allocated to the transmit-FIFO. The default number is 128 bytes. (R/W)
- **UART_RX_SIZE**: This register is used to configure the amount of memory allocated to the receive-FIFO. The default number is 128 bytes. (R/W)

**UART_MEM_PD**: Set this bit to power down the memory. When the `reg_mem_pd` register is set to 1 for all UART controllers, Memory will enter the low-power mode. (R/W)

---

### Register 19.24. UART_MEM_TX_STATUS_REG (0x5c)

| Field | Offset |
|-------|--------|
| (reserved) | - |
| UART_MEM_TX_WR_ADDR | 31-24 |
| UART_MEM_TX_RD_ADDR | 23-0 |

**Description:**

- **UART_MEM_TX_WR_ADDR**: Represents the offset address to write TX FIFO. (RO)
- **UART_MEM_TX_RD_ADDR**: Represents the offset address to read TX FIFO. (RO)

---

*Espressif Systems*
*Submit Documentation Feedback*

ESP32 TRM (Version 5.6)