

```markdown
| 1 | ISP (ISP-to-memory) |
|----|---------------------|
| 2 | ISP (memory-to-ISP) |

For more information about ISP and MIPI DSI, please refer to Chapter 36 Image Signal Processor (ISP) and Chapter 4 MIPI DSI [to be added later].
```

## 5.5 Functional Description

This section provides a detailed description of the key features and operations of the module.

### 5.5.1 Transfer Hierarchy

Transfers are organized into a maximum of four levels: DMA transfer level, block transfer level, transaction level, and AXI transfer level.

Figure 5.5-1 shows four transfer levels between VDMA and peripherals.

Figure 5.5-2 shows three transfer levels between VDMA and memory. There is no transaction level because memory is assumed to be always ready for data transfer.

The following descriptions of DMA, block, and AXI transfers apply to the transfer between VDMA and memory, VDMA and peripherals. The description of the transaction level applies only to transfers between VDMA and peripherals.

*   **DMA transfer**: Software defines the number of blocks in a DMA transfer. Once a DMA transfer has finished, VDMA disables the channel and generates an interrupt. The channel can then be reprogrammed for a new DMA transfer. A DMA transfer can consist of either a single-block or a multi-block transfer.
*   **Block transfer**: A block transfer moves a specified data block through the VDMA. The flow controller controls the block length. There are two types of block transfer: single-block transfer and multi-block transfer. As shown in Figure 5.5-1, a block transfer may consist of multiple transactions.
    *   **Transaction**: A peripheral request may trigger either a single or burst transaction, corresponding to an AXI single transfer or multiple AXI burst transfers, respectively.
        - Single transaction: The length of a single transaction is always 1, in the unit of `DMAC_CHn_SRC_TR_WIDTH`.
        - Burst transaction: The length of a burst transaction is programmed into the VDMA through `DMAC_CHn_SRC_MSIZE` for the source or `DMAC_CHn_DST_MSIZE` for the destination. The burst length typically relates to the FIFO sizes in the source or destination peripherals. For more information, please refer to the chapter on each peripheral.
    *   **AXI transfer**: Refers to the AXI protocol transfer, which is divided into AXI single transfer and AXI burst transfer.
```