
```markdown
- reserved (DWO) [29]: Reserved. The value of this bit does not matter.
- err_eof (DWO) [28]: Specifies whether the received data has errors.
  0: The received data does not have errors.
  1: The received data has errors.
  This bit is used only when UHCI or PARLIO uses GDMA to receive data. When an error is detected in the received data segment corresponding to a descriptor, this bit in the receive descriptor is set to 1 by hardware.
- reserved (DWO) [27:24]: Reserved.
- length (DWO) [23:12]: Specifies the number of valid bytes in the buffer that this descriptor points to. This field in a transmit descriptor is written by software and indicates how many bytes can be read from the buffer; this field in a receive descriptor is written by hardware automatically and indicates how many valid bytes have been stored into the buffer.
- size (DWO) [11:0]: Specifies the size of the buffer that this descriptor points to.
- buffer address pointer (DW1): Address of the buffer. This field can only point to internal RAM.
- next descriptor address (DW2): Address of the next descriptor. If the current descriptor is the last one, this value could be 0. This field can only point to internal RAM.

If the length of data received is smaller than the size of the buffer, the GDMA controller will not use the available space of the buffer in the next transaction.

## 3.4.2 Peripheral-to-Memory and Memory-to-Peripheral Data Transfer

The GDMA controller can transfer data from memory to peripheral (transmit) and from peripheral to memory (receive). A transmit channel transfers data in the specified memory location to a peripheral’s transmitter via an outlinkn, whereas a receive channel transfers data received by a peripheral to the specified memory location via an inlinkn.

Every transmit and receive channel can be connected to any peripheral with the GDMA feature. Table 3.4-1 illustrates how to select the peripheral to be connected via registers. "Dummy-n" corresponds to register values for memory-to-memory data transfer. When a channel is connected to a peripheral, the rest channels cannot be connected to that peripheral.

Table 3.4-1. Selecting Peripherals via Register Configuration

| GDMA_PERI_IN_SEL_CHn | Peripheral |
|----------------------|----------|
| GDMA_PERI_OUT_SEL_CHn |          |
| 0                    | SPI2     |
| 1                    | Dummy-1  |
| 2                    | UHCI     |
| 3                    | I2S      |
| 4                    | Dummy-4  |
| 5                    | Dummy-5  |
| 6                    | AES      |
| 7                    | SHA      |
| 8                    | ADC      |
```