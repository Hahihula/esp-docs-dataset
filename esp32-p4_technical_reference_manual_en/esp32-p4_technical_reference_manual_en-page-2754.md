

```markdown
Register 54.11. SDHOST_FIFOTH_REG (0x004C)

| Bit | 31 | 30 | 28 | 27 | 26 | 16 | 15 | 12 | 11 | 0 |
|-----|----|----|----|----|----|----|----|----|----|---|
|     |    |    |    |    |    |    |    |    |    | Reset |
| Value | 0 | 0x0 | 0 | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 |

SDHOST_TX_WMARK Configures FIFO threshold watermark level when transmitting data to card. When FIFO data count is less than or equal to this number, DMA/FIFO request is raised. During end of packet, request or interrupt is generated, regardless of threshold programming. In non-DMA mode, when transmitting FIFO threshold (TXDR) interrupt is enabled, then interrupt is generated instead of DMA request. During end of packet, on last interrupt, host is responsible for filling FIFO with only the required remaining bytes (not before FIFO is full or after CIU completes data transfers, because FIFO may not be empty). In DMA mode, at end of packet, if last transfer is less than burst size, DMA controller does single cycles until required bytes are transferred. (R/W)

SDHOST_RX_WMARK Configures FIFO threshold watermark level when receiving data from card. When FIFO data count reaches greater than this number, DMA/FIFO request is raised. During end of packet, request is generated regardless of threshold programming in order to complete any remaining data. In non-DMA mode, when receiver FIFO threshold (RXDR) interrupt is enabled, then interrupt is generated instead of DMA request. During end of packet, interrupt is not generated if threshold programming is larger than any remaining data. It is responsibility of host to read remaining bytes on seeing Data Transfer Done interrupt. In DMA mode, at end of packet, even if remaining bytes are less than threshold, DMA request does single transfers to flush out any remaining bytes before Data Transfer Done interrupt is set. (R/W)

SDHOST_DMA_MULTIPLE_TRANSACTION_SIZE Configures burst size of multiple transaction, should be programmed same as DMA controller multiple-transaction-size SD-HOST_SRC/DEST_MSIZE.
Ox0: 1-byte transfer
Ox1: 4-byte transfer
Ox2: 8-byte transfer
Ox3: 16-byte transfer
Ox4: 32-byte transfer
Ox5: 64-byte transfer
Ox6: 128-byte transfer
Ox7: 256-byte transfer
(R/W)
```