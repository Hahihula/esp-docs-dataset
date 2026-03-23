

```markdown
## 32.7 Registers

The addresses in this section are relative to USB Serial/JTAG controller base address provided in Table 5.3-2 in Chapter 5 System and Memory.

Register 32.1. USB_SERIAL_JTAG_EP1_REG (0x0000)

USB_SERIAL_JTAG_PWR_BYTE Write or read byte data to or from UART TX/RX FIFO.
When `USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT` is set, users can write data (up to 64 bytes) into UART TX FIFO through this register.
When `USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT` is set, users can check how many data is received through `USB_SERIAL_JTAG_OUT_EP1_WR_ADDR`, then read data from UART RX FIFO through this register.
(R/W)
```