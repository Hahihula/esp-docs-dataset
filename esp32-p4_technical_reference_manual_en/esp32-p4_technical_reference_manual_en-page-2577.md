

```markdown
Register 51.2. USB_SERIAL_JTAG_EP1_CONF_REG (0x0004)
```

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 3   | reserved                                   |                                                                             |
| 2   | USB_SERIAL_JTAG_OUT_EP_DATA_AVAIL          | Represents whether there is data in CDC-ACM RX FIFO.                        |
| 1   | USB_SERIAL_JTAG_IN_EP_DATA_FREE            | Represents whether CDC-ACM TX FIFO has space available.                     |
| 0   | USB_SERIAL_JTAG_WR_DONE                    | Configures whether to represent writing byte data to CDC-ACM TX FIFO is done.|

**USB_SERIAL_JTAG_WR_DONE**  
Configures whether to represent writing byte data to CDC-ACM TX FIFO is done.

- 0: No effect
- 1: Represents writing byte data to CDC-ACM TX FIFO is done. This bit then stays 0 until data in CDC-ACM TX FIFO is read by the USB Host (WT)

**USB_SERIAL_JTAG_IN_EP_DATA_FREE**  
Represents whether CDC-ACM TX FIFO has space available.

- 0: CDC-ACM TX FIFO is full and no data should be written into it
- 1: CDC-ACM TX FIFO is not full and data can be written into it

After writing `USB_SERIAL_JTAG_WR_DONE`, this bit will be 0 until data in CDC-ACM TX FIFO is read by USB Host. (RO)

**USB_SERIAL_JTAG_OUT_EP_DATA_AVAIL**  
Represents whether there is data in CDC-ACM RX FIFO.

- 0: There is no data in CDC-ACM RX FIFO
- 1: There is data in CDC-ACM RX FIFO (RO)
```