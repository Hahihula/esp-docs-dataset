

```markdown
## 2.4.4 Enabling GDMA

Software uses the GDMA controller through linked lists. When the GDMA controller receives data, software loads an inlink, configures `GDMA_INLINK_ADDR_CHn` field with address of the first receive descriptor, and sets `GDMA_INLINK_START_CHn` bit to enable GDMA. When the GDMA controller transmits data, software loads an outlink, prepares data to be transmitted, configures `GDMA_OUTLINK_ADDR_CHn` field with address of the first transmit descriptor, and sets `GDMA_OUTLINK_START_CHn` bit to enable GDMA. `GDMA_INLINK_START_CHn` bit and `GDMA_OUTLINK_START_CHn` bit are cleared automatically by hardware.

In some cases, you may want to append more descriptors to a DMA transfer that is already started. Naively, it would seem to be possible to do this by clearing the EOF bit of the final descriptor in the existing list and setting its next descriptor address pointer field (DW2) to the first descriptor of the to-be-added list. However, this strategy fails if the existing DMA transfer is almost or entirely finished. Instead, the GDMA engine has specialized logic to make sure a DMA transfer can be continued or restarted: if it is still ongoing, it will make sure to take the appended descriptors into account; if the transfer has already finished, it will restart with the new descriptors. This is implemented in the Restart function.

When using the Restart function, software needs to rewrite address of the first descriptor in the new list to DW2 of the last descriptor in the loaded list, and set `GDMA_INLINK_RESTART_CHn` bit or `GDMA_OUTLINK_RESTART_CHn` bit (these two bits are cleared automatically by hardware). As shown in Figure 2.4-2, by doing so hardware can obtain the address of the first descriptor in the new list when reading the last descriptor in the loaded list, and then read the new list.

Figure 2.4-2. Relationship among Linked Lists

## 2.4.5 Linked List Reading Process

Once configured and enabled by software, the GDMA controller starts to read the linked list from internal RAM. The GDMA performs checks on descriptors in the linked list. Only if descriptors pass the checks, will the corresponding GDMA channel transfer data. If the descriptors fail any of the checks, hardware will trigger descriptor error interrupt (either `GDMA_IN_DSCR_ERR_CHn_INT` or `GDMA_OUT_DSCR_ERR_CHn_INT`), and the channel will halt.

The checks performed on descriptors are:

*   Owner bit check when `GDMA_IN_CHECK_OWNER_CHn` or `GDMA_OUT_CHECK_OWNER_CHn` is set to 1.
```