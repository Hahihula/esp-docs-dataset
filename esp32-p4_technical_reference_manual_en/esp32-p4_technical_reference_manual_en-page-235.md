

```markdown
In some cases, you may want to append more descriptors to a DMA transfer that is already started. Naively, it would seem to be possible to do this by clearing the EOF bit of the final descriptor in the existing list and setting its next descriptor address pointer field (DW2) to the first descriptor of the to-be-added list. However, this strategy fails if the existing DMA transfer is almost or entirely finished. Instead, the GDMA controller has specialized logic to make sure a DMA transfer can be continued or restarted: if the transfer is ongoing, the controller will make sure to take the appended descriptors into account; if the transfer has already finished, the controller will restart with the new descriptors. This is implemented by the Restart function.

When using the Restart function, software needs to rewrite the address of the first descriptor in the new list to DW2 of the last descriptor in the loaded list, and set AHB/AXI_DMA_INLINK_RESTART_CHn bit or AHB/AXI_DMA_OUTLINK_RESTART_CHn bit (these two bits are cleared automatically by hardware). As shown in Figure 4.4-2, by doing so hardware can obtain the address of the first descriptor in the new list when reading the last descriptor in the loaded list, and then read the new list.

Figure 4.4-2. Relationship among Linked Lists

## 4.4.5 Linked List Reading Process

Once configured and enabled by software, the GDMA controller starts to read the linked list from memory. The GDMA performs checks on descriptors in the linked list. Only if descriptors pass the checks, the corresponding GDMA channel will start data transfer. If the descriptors fail any of the checks, hardware will trigger descriptor error interrupt (either AHB/AXI_DMA_IN_DSCR_ERR_CHn_INT or AHB/AXI_DMA_OUT_DSCR_ERR_CHn_INT), and the channel will halt.

The checks performed on descriptors are:

*   Owner bit check when AHB/AXI_DMA_IN_CHECK_OWNER_CHn or AHB/AXI_DMA_OUT_CHECK_OWNER_CHn is set to 1. If the owner bit is 0, the buffer is accessed by the CPU. In this case, the owner bit fails the check. The owner bit will not be checked if AHB/AXI_DMA_IN_CHECK_OWNER_CHn or AHB/AXI_DMA_OUT_CHECK_OWNER_CHn is 0.
*   Descriptor address check, which checks if the descriptor address is located in configured memory space. If a GDMA-AHB descriptor points to AHB_DMA_ACCESS_INTR_MEM_START_ADDR ~ AHB_DMA_ACCESS_INTR_MEM_END_ADDR, it passes the check. If a GDMA-AXI descriptor points to AXI_DMA_ACCESS_INTR_MEM_START_ADDR ~ AXI_DMA_ACCESS_INTR_MEM_END_ADDR, or AXI_DMA_ACCESS_EXTR_MEM_START_ADDR ~ AXI_DMA_ACCESS_EXTR_MEM_END_ADDR, it passes
```