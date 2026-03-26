

```markdown
Chapter 5 VDMA Controller (VDMA)
GoBack

5.5.2.2 Write Arbiter

The write arbiter arbitrates write requests, including:

*   Destination Data Write Request
*   LLI Descriptor Write-Back Request

The block diagram of the write arbiter is shown in Figure 5.5-4:

Figure 5.5-4. VDMA Write Arbiter

Within the same channel, Destination Data Write Request has higher priority than LLI Descriptor Write-Back Request. If different channels have the same priority, then Data Write Requests have the highest priority.

5.5.3 Handshaking Interface

A peripheral uses a handshaking interface to inform VDMA that it is ready to transmit or receive data via AXI bus. The operation of the handshaking interface depends on whether the flow controller is the peripheral or VDMA.

VDMA performs a single transaction or a burst transaction per handshake. In some cases, a block transfer cannot be completed using only burst transactions. This situation typically occurs when the block size is not a multiple of the burst transaction length. In this case, the block transfer uses burst transactions until the remaining size of the block is less than the amount of data in the burst transaction. At this point, a single transaction is used to complete the block transfer.

A source’s burst transaction size is determined by `DMAC_CHn_SRC_MSIZE`. A destination’s burst transaction size is determined by `DMAC_ChN_DST_MSIZE`. The transaction size also corresponds to the burst transaction size used for handshaking. The value of `DMAC_CHn_SRC_MSIZE` or `DMAC_ChN_DST_MSIZE` should match the peripheral configuration. For detailed information, please refer to the chapter on related peripherals.
```