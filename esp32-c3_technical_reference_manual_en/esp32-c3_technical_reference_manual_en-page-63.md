

```markdown
- Reserved (DW0) [27:24]: Reserved.
- Length (DW0) [23:12]: Specifies the number of valid bytes in the buffer that this descriptor points to. This field in a transmit descriptor is written by software and indicates how many bytes can be read from the buffer; this field in a receive descriptor is written by hardware automatically and indicates how many valid bytes have been stored into the buffer.
- Size (DW0) [11:0]: Specifies the size of the buffer that this descriptor points to.
- Buffer address pointer (DW1): Address of the buffer. This field can only point to internal RAM.
- Next descriptor address (DW2): Address of the next descriptor. If the current descriptor is the last one, this value is 0. This field can only point to internal RAM.

If the length of data received is smaller than the size of the buffer, the GDMA controller will not use the available space of the buffer in the next transaction.
```

## 2.4.2 Peripheral-to-Memory and Memory-to-Peripheral Data Transfer

The GDMA controller can transfer data from memory to peripheral (transmit) and from peripheral to memory (receive). A transmit channel transfers data in the specified memory location to a peripheral’s transmitter via an `outlinkn`, whereas a receive channel transfers data received by a peripheral to the specified memory location via an `inlinkn`.

Every transmit and receive channel can be connected to any peripheral with GDMA feature. Table 2.4-1 illustrates how to select the peripheral to be connected via registers. When a channel is connected to a peripheral, the rest channels can not be connected to that peripheral.

Table 2.4-1. Selecting Peripherals via Register Configuration

| GDMA_PERI_IN_SEL_CHn | GDMA_PERI_OUT_SEL_CHn | Peripheral |
|----------------------|------------------------|------------|
|                      |                        |            |
| 0                    |                        | SPI2       |
| 1                    |                        | Reserved   |
| 2                    |                        | UHCIO      |
| 3                    |                        | I2S        |
| 4                    |                        | Reserved   |
| 5                    |                        | Reserved   |
| 6                    |                        | AES        |
| 7                    |                        | SHA        |
| 8                    |                        | ADC        |
| 9 ~ 63               |                        | Invalid    |

## 2.4.3 Memory-to-Memory Data Transfer

The GDMA controller also allows memory-to-memory data transfer. Such data transfer can be enabled by setting `GDMA_MEM_TRANS_EN_CHn`, which connects the output of transmit channel n to the input of receive channel n. Note that a transmit channel is only connected to the receive channel with the same number (n).
```