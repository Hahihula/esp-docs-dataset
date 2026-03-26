

```markdown
## Note:
LP-SPI does not support this transfer. The description below is for GP-SPI only.
```

DMA-controlled transfer refers to the transfer in which the DMA RX module receives data and the DMA TX module sends data. This transfer is supported both as master and as slave.

A DMA-controlled transfer can be:

*   a single transfer, consisting of only one transaction. GP-SPI supports this transfer both as master and as slave.
*   a configurable segmented transfer, consisting of several transactions (segments). Only GP-SPI2 supports this transfer when working as a master. For more information, see Section 43.5.9.5.
*   a slave segmented transfer, consisting of several transactions (segments). GP-SPI supports this transfer only when working as a slave. For more information, see Section 43.5.10.3.

A DMA-controlled transfer only needs to be triggered once by CPU. When such a transfer is triggered, data is transferred by the DMA engine from or to the DMA-linked memory, without CPU operation.

DMA-controlled transfer supports full-duplex communication, half-duplex communication and functions described in Section 43.5.9 and Section 43.5.10. Meanwhile, the DMA RX module is independent from the DMA TX module, which means that there are four kinds of full-duplex communications:

*   Data is received in DMA-controlled mode and sent in DMA-controlled mode.
*   Data is received in DMA-controlled mode but sent in CPU-controlled mode.
*   Data is received in CPU-controlled mode but sent in DMA-controlled mode.
*   Data is received in CPU-controlled mode and sent in CPU-controlled mode.

### 43.5.7.1 DMA Configuration

*   Select a DMA channel `n` and configure DMA TX/RX descriptor. See Chapter 4 GDMA Controller (GDMA-AHB, GDMA-AXI).
```