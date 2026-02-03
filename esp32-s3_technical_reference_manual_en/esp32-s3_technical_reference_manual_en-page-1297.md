**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

**Register Information Table Header:**
- Register Name | Offset in Word/Byte | Description
- SDHOST_DMA_ML_TRANSACTION_SIZE | 0x0040 | Reserved.
- SDHOST_RX_WMARK | 0x0050 | FIFO threshold watermark level when receiving data to card. When FIFO data count reaches greater than this number, DMA/FIFO request is raised.

**Register Description:**
SDHOST_DMA_ML_TRANSACTION_SIZE - Burst size of multiple transaction should be programmed same as DMA controller multiple-transaction-size SDHOST_SRC/DEST_MSIZE. (R/W)

- 000: 1-byte transfer;
- 001: 4-byte transfer;
- 010: 8-byte transfer;
- 011: 16-byte transfer;
- 100: 32-byte transfer;
- 101: 64-byte transfer;
- 110: 128-byte transfer;
- 111: 256-byte transfer.

SDHOST_RX_WMARK - FIFO threshold watermark level when receiving data to card. When FIFO data count reaches greater than this number, DMA/FIFO request is raised.
During end of packet, request is generated regardless of threshold programming in order to complete any remaining data. In non-DMA mode, when receiver FIFO threshold (RXDR) interrupt is enabled, then interrupt is generated instead of DMA request.

**Additional Information:**
- During the end of a packet, if the threshold count reaches greater than this number and RXDR interrupt is not set before the last byte transfer completes.
- It's responsibility to host to read remaining bytes on seeing Data Transfer Done interrupt. In DMA mode at the end of packets even when there are less than threshold bytes.

**SDHOST_TX_WMARK - FIFO Threshold Watermark Level:**
When transmitting data, if FIFO data count is equal or greater and RXDR interrupt occurs.
During packet transmission:
- If RXDR interrupt enabled then interrupt generated regardless
- In non-DMA mode host responsible for filling FIFO with remaining required transfer

**Footer Information:** 
Espressif Systems | ESP32-S3 TRM (Version 1.7)