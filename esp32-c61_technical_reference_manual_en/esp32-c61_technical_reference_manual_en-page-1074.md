

# 29.7 Registers

The addresses in this section are relative to USB Serial/JTAG controller base address provided in Table 4.3-2 in Chapter 4 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 29.1. USB_SERIAL_JTAG_EP1_REG (0x0000)

```
31                                 8 7                 0
+-----------------------------------------------+
|             (reserved)            | Oxo |
+--------------------------------------- Reset
```

**USB_SERIAL_JTAG_RDWR_BYTE** A write to this register pushes the written data into the CDC TX FIFO; a read from this register pops a byte from the CDC RX FIFO and returns it.

When `USB_SERIAL_JTAG_SERIAL_IN_EMPTY_INT` is set, users can write data (up to 64 bytes) into CDC-ACM TX FIFO through this register.

When `USB_SERIAL_JTAG_SERIAL_OUT_RECV_PKT_INT` is set, users can check how many data is received through `USB_SERIAL_JTAG_OUT_EP1_WR_ADDR`, then read data from CDC-ACM RX FIFO through this register. (R/W)