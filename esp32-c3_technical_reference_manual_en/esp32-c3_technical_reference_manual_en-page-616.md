

```markdown
Note:

* TX/RX data address mentioned above both are byte-addressable. Address 0 stands for `SPI_WO_REG[7:0]`, and Address 1 for `SPI_WO_REG[15:8]`, and so on. The largest address is `SPI_W15_REG[31:24]`.
* To avoid any possible error in TX/RX data, such as TX data being sent more than once or RX data being overwritten, please make sure the registers are configured correctly.

## 27.5.5.2 CPU-Controlled Slave Mode

In a CPU-controlled slave full-duplex or half-duplex transfer, the RX data or TX data is saved to or sent from `SPI_WO_REG ~ SPI_W15_REG`, which are byte-addressable.

* In full-duplex communication, the address of `SPI_WO_REG ~ SPI_W15_REG` starts from 0 and is incremented by 1 on each byte transferred. If the data address is larger than 63, the content of `SPI_W15_REG[31:24]` is overwritten.
* In half-duplex communication, the ADDR value in transmission format is the start address of the RX or TX data, corresponding to the registers `SPI_WO_REG ~ SPI_W15_REG`. The RX or TX address is incremented by 1 on each byte transferred. If the address is larger than 63 (the highest byte address, i.e. `SPI_W15_REG[31:24]`), the address of overflowing data is always 63 and only the content of `SPI_W15_REG[31:24]` is overwritten.

According to your applications, the registers `SPI_WO_REG ~ SPI_W15_REG` can be used as:

* data buffers only
* data buffers and status buffers
* status buffers only

## 27.5.6 DMA-Controlled Data Transfer

DMA-controlled transfer refers to the transfer, in which GDMA RX module receives data and GDMA TX module sends data. This transfer is supported both in master mode and in slave mode.

A DMA-controlled transfer can be:

* a single transfer, consisting of only one transaction. GP-SPI2 supports this transfer both in master and slave modes.
* a configurable segmented transfer, consisting of several transactions (segments). GP-SPI2 supports this transfer only in master mode. For more information, see Section 27.5.8.5.
* a slave segmented transfer, consisting of several transactions (segments). GP-SPI2 supports this transfer only in slave mode. For more information, see Section 27.5.9.3.

A DMA-controlled transfer only needs to be triggered once by CPU. When such transfer is triggered, data is transferred by the GDMA engine from or to the DMA-linked memory, without CPU operation.

DMA-controlled mode supports full-duplex communication, half-duplex communication and functions described in Section 27.5.8 and Section 27.5.9. Meanwhile, the GDMA RX module is independent from the GDMA TX module, which means that there are four kinds of full-duplex communications:

* Data is received in DMA-controlled mode and sent in DMA-controlled mode.
```