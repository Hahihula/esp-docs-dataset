

```markdown
## 28.5.5.2 CPU-Controlled Slave Transfer

In a CPU-controlled slave full-duplex or half-duplex transfer, the RX data or TX data is saved to or sent from `SPI_W0_REG ~ SPI_W15_REG`, which are byte-addressable.

* In full-duplex communication, the address of `SPI_W0_REG ~ SPI_W15_REG` starts from 0 and is incremented by 1 on each byte transferred. If the data address is larger than 63, the data in `SPI_W0_REG ~ SPI_W15_REG` will be overwritten, same as the behaviors described in the master mode when high part mode is disabled.
* In half-duplex communication, the `ADDR` value in transmission format is the start address of the RX or TX data, corresponding to the registers `SPI_W0_REG ~ SPI_W15_REG`. The RX or TX address is incremented by 1 on each byte transferred. If the address is larger than 63 (the highest byte address, i.e., `SPI_W15_REG[31:24]`), the data in `SPI_W8_REG ~ SPI_W15_REG` will be overwritten, same as the behaviors described in the master mode when high part mode is enabled.

According to your applications, the registers `SPI_W0_REG ~ SPI_W15_REG` can be used as:

* data buffers only
* data buffers and status buffers
* status buffers only

## 28.5.6 DMA-Controlled Data Transfer

DMA-controlled transfer refers to the transfer in which the GDMA RX module receives data and the GDMA TX module sends data. This transfer is supported both as master and as slave.

A DMA-controlled transfer can be:

* a single transfer, consisting of only one transaction. GP-SPI2 supports this transfer both as master and as slave.
* a configurable segmented transfer, consisting of several transactions (segments). GP-SPI2 supports this transfer only as master. For more information, see Section 28.5.8.5.
* a slave segmented transfer, consisting of several transactions (segments). GP-SPI2 supports this transfer only as slave. For more information, see Section 28.5.9.3.

A DMA-controlled transfer only needs to be triggered once by CPU. When such a transfer is triggered, data is transferred by the GDMA engine from or to the DMA-linked memory, without CPU operation.

DMA-controlled transfer supports full-duplex communication, half-duplex communication and functions described in Section 28.5.8 and Section 28.5.9. Meanwhile, the GDMA RX module is independent from the GDMA TX module, which means that there are four kinds of full-duplex communications:

* Data is received in DMA-controlled mode and sent in DMA-controlled mode.
* Data is received in DMA-controlled mode but sent in CPU-controlled mode.
* Data is received in CPU-controlled mode but sent in DMA-controlled mode.
* Data is received in CPU-controlled mode and sent in CPU-controlled mode.
```