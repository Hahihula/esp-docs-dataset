

```markdown
## 30.6 Registers

The addresses in this section are relative to USB Serial/JTAG Controller base address provided in Table 3.3-3 in Chapter 3 System and Memory.

Register 30.1. USB_SERIAL_JTAG_EP1_REG (0x0000)

USB_SERIAL_JTAG_RDWR_BYTE Write and read byte data to/from UART Tx/Rx FIFO through this field. When USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT is set then user can write data (up to 64 bytes) into UART Tx FIFO. When USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT is set, user can check USB_SERIAL_JTAG_OUT_EP1_WR_ADDR and USB_SERIAL_JTAG_OUT_EP1_RD_ADDR to know how many data is received, then read that amount of data from UART Rx FIFO. (R/W)
```