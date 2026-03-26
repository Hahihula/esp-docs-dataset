

```markdown
Chapter 5 VDMA Controller (VDMA)

VDMA has three hardware handshaking interfaces with MIPI DSI, ISP (ISP-to-memory), and ISP (memory-to-ISP). For the mapping relationship please see Table 5.4-1.

5.5.4 Transfer Control

Transfer control logic facilitates the data transfer from a source to a destination. Data from the source is temporarily stored in the channel FIFO before being sent to the destination. If source and destination peripherals use different transfer sizes, VDMA will pack and unpack the data to fit the FIFO configuration.

For a specific DMA transfer, the transfer type and flow control configurations are determined by DMAC_CHn_TT_FC.

5.5.4.1 Single-Block Transfer

If a DMA transfer consists of a single block, the software can set DMAC_CHn_SRC_MULTBLK_TYPE and DMAC_CHn_DST_MULTBLK_TYPE to 0 to enable contiguous-address-based single-block transfer. In this case, VDMA disables the channel once the block transfer of size DMAC_CHn_BLOCK_TS is completed.

Note:
Single-block transfer is a special case of multi-block transfer, and there is no strict distinction between the two. In this chapter, single-block transfer refers to the transfer consisting of only one block, while multi-block transfer refers to the transfer consisting of at least two blocks.

5.5.4.2 Multi-Block Transfer

If a DMA transfer consists of multiple blocks, the software can configure DMAC_CHn_SRC_MULTBLK_TYPE and DMAC_CHn_DST_MULTBLK_TYPE to choose a multi-block transfer type. There are four types of multi-block transfers, depending on how the transfer control registers (DMAC_CHn_SARO_REG, DMAC_CHn_DARO_REG, DMAC_CHn_BLOCK_TS, DMAC_CHn_CTLO/1_REG) are updated:

1. Contiguous address
2. Auto reloading: Register values reload from initial values
3. Shadow register: Register values load from shadow registers
4. Linked list Register values load from the next linked list (LLI)

Table 5.5-1 lists all the cases of register update methods for multi-block transfer.
```