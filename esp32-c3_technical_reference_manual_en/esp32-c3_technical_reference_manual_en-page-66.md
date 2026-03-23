

```markdown
Table 2.4-2 lists the requirements for descriptor field alignment when accessing internal RAM.

When burst mode is disabled, size, length, and buffer address pointer in both transmit and receive descriptors do not need to be word-aligned. That is to say, GDMA can read data of specified length (1 ~ 4095 bytes) from any start addresses in the accessible address range, or write received data of the specified length (1 ~ 4095 bytes) to any contiguous addresses in the accessible address range.

When burst mode is enabled, size, length, and buffer address pointer in transmit descriptors are also not necessarily word-aligned. However, size and buffer address pointer in receive descriptors except length should be word-aligned.

## 2.4.8 Arbitration

To ensure timely response to peripherals running at a high speed with low latency (such as SPI), the GDMA controller implements a fixed-priority channel arbitration scheme. That is to say, each channel can be assigned a priority from 0 ~ 9. The larger the number, the higher the priority, and the more timely the response. When several channels are assigned the same priority, the GDMA controller adopts a round-robin arbitration scheme.

Please note that the overall throughput of peripherals with GDMA feature not exceed the maximum bandwidth of the GDMA, so that requests from low-priority peripherals can be responded to.

## 2.5 GDMA Interrupts

*   DMA_INFIFO_OVF_CHn_INT: Triggered when the RX FIFO of GDMA overflows.
*   GDMA_INFIFO_UDF_CHn_INT: Triggered when the RX FIFO of GDMA underflows.
*   GMA_OUTFIFO_OVF_CHn_INT: Triggered when the TX FIFO of GDMA overflows.
*   GDMA_OUTFIFO_UDF_CHn_INT: Triggered when the TX FIFO of GDMA underflows.
*   GDMA_OUT_TOTAL_EOF_CHn_INT: Triggered when all data corresponding to a linked list (including multiple descriptors) has been sent via transmit channel n.
*   GDMA_IN_DSCR_EMPTY_CHn_INT: Triggered when the size of the buffer pointed by receive descriptors is smaller than the length of data to be received via receive channel n.
*   GDMA_OUT_DSCR_ERR_CHn_INT: Triggered when an error is detected in a transmit descriptor on transmit channel n.
*   GDMA_IN_DSCR_ERR_CHn_INT: Triggered when an error is detected in a receive descriptor on receive channel n.
*   GDMA_OUT_EOF_CHn_INT: Triggered when EOF in a transmit descriptor is 1 and data corresponding to this descriptor has been sent via transmit channel n. If GDMA_OUT_EOF_MODE_CHn is 0, this interrupt will be triggered when the last byte of data corresponding to this descriptor enters GDMA's transmit channel; if GDMA_OUT_EOF_MODE_CHn is 1, this interrupt is triggered when the last byte of data is taken from GDMA's transmit channel.
```