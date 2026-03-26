

```markdown
has specialized logic to make sure a transfer can be continued or restarted: if the transfer is ongoing, the controller will make sure to take the appended descriptors into account; if the transfer has already finished, the controller will restart with the new descriptors. This is implemented by the Restart function.

When using the Restart function, software needs to

1. Set `DMA2D_INLINK_STOP_CHn` or `DMA2D_OUTLINK_STOP_CHn` to stop the 2D-DMA when it finishes processing the current descriptor
2. Rewrite the address of the first descriptor in the new list to DW4 of the last descriptor in the loaded list
3. Set `DMA2D_INLINK_RESTART_CHn` or `DMA2D_OUTLINK_RESTART_CHn` (these two bits are cleared automatically by hardware)

By doing so, hardware can obtain the address of the first descriptor in the new list when reading the last descriptor in the loaded list, and then read the new list.

## 6.4.9 Linked List Reading Process

Once configured and enabled by software, the 2D-DMA controller starts to read the linked list from the memory. The 2D-DMA performs checks on descriptors in the linked list. Only if descriptors pass the checks, the corresponding 2D-DMA channel will start data transfer. If the descriptors fail any of the checks, hardware will trigger descriptor error interrupt (either `DMA2D_IN_DSCR_ERR_CHn_INT` or `DMA2D_OUT_DSCR_ERR_CHn_INT`), and the channel will remain idle. This channel can be restarted by setting `DMA2D_OUTLINK_START_CHn` or `DMA2D_INLINK_START_CHn` again.

The checks performed on descriptors are:

* Owner bit check when `DMA2D_IN_CHECK_OWNER_CHn` or `DMA2D_OUT_CHECK_OWNER_CHn` is set to 1. If the owner bit is 0, the buffer is accessed by the CPU. In this case, the owner bit fails the check. The owner bit will not be checked if `DMA2D_IN_CHECK_OWNER_CHn` or `DMA2D_OUT_CHECK_OWNER_CHn` is 0.
* Descriptor address check, which checks if the descriptor address is located in configured memory space. If a 2D-DMA descriptor points to `DMA2D_ACCESS_INTR_MEM_START_ADDR ~ DMA2D_ACCESS_INTR_MEM_END_ADDR` (the value should be located in internal memory) or `DMA2D_ACCESS_EXTR_MEM_START_ADDR ~ DMA2D_ACCESS_EXTR_MEM_END_ADDR` (the value should be located in external memory), it passes the check. For details, please refer to Section 6.4.11.
* HA/VA/hb/vb/SIZE check, which checks if any of these fields is 0. If any field is 0, it fails the check. HA/VA/hb/vb fields are not checked in 1D mode, while SIZE is checked only in 1D mode.

After the software detects a descriptor error interrupt, it must reset the corresponding channel, and restart the 2D-DMA DMA by setting the `DMA2D_OUTLINK_START_CHn` or `DMA2D_INLINK_START_CHn` bit.

To quickly obtain receive or transmit descriptors from the memory, AXI burst transfers for 2D-DMA can be enabled by setting `DMA2D_INDSCR_BURST_EN_CHn` or `DMA2D_OUTDSCR_BURST_EN_CHn`.

## 6.4.10 EOF

**Note:** In this chapter, EOF of transmit descriptors refers to eof (i.e., bit 30 of DWO), while EOF of receive descriptors refers to both eof and err_eof (i.e., bit 28 of DWO).

The 2D-DMA controller uses EOF (end of frame) flags to indicate the end of the image transmission.
```