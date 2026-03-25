
```markdown
- UART_WK_MODE_SEL = 2: When the UART receiver detects a start bit, the chip will be woken up.
- UART_WK_MODE_SEL = 3: When the UART receiver receives a specific character sequence, the chip will be woken up. The wakeup characters can be defined by configuring UART_WK_CHAR0, UART_WK_CHAR1, UART_WK_CHAR2, UART_WK_CHAR3, and UART_WK_CHAR4. These characters can be formed into different character sequences by configuring UART_CHAR_NUM and UART_WK_CHAR_MASK, as shown in Table 32.4-1. Once the sequence is detected, the chip will be woken up. For the last configuration in Table 32.4-1, UART will detect for CHAR0 ~ CHAR4 in order.

Table 32.4-1. UART_CHAR_WAKEUP Mode Configuration

| UART_CHAR_NAME | UART_WP_CHAR_MASK | Character Sequence |
|----------------|-------------------|--------------------|
| 1              | 0xF               | CHAR4              |
| 2              | 0x7               | CHAR3/CHAR4        |
| 3              | 0x3               | CHAR2/CHAR3/CHAR4  |
| 4              | 0x1               | CHAR1/CHAR2/CHAR3/CHAR4 |
| 5              | 0x0               | CHAR0/CHAR1/CHAR2/CHAR3/CHAR4 |

After the chip is woken up by UART, it is necessary to clear the wake_up signal by transmitting data to UART in Active mode or resetting the whole UART, otherwise the number of rising edges required for the next wakeup will be reduced.

## 32.4.9 Flow Control

UART controllers have two ways to control data flow, namely hardware flow control and software flow control. Hardware flow control is achieved using output signal rtsn_out and input signal ctsn_in. Software flow control is achieved by inserting special characters in the data flow sent and detecting special characters in the data flow received.

### 32.4.9.1 Hardware Flow Control

Figure 32.4-8 shows the hardware flow control of a UART controller. Hardware flow control uses output signal rtsn_out and input signal dsn_in. Figure 32.4-9 illustrates how these signals are connected between UART on ESP32-C5 (hereinafter referred to as IUO) and the external UART (hereinafter referred to as EUO).
```