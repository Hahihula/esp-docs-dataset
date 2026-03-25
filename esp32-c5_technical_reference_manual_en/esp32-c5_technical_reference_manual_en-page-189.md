

```markdown
The last descriptor of linked list

Next descriptor address

New linked list

Next descriptor address

Figure 5.4-2. Relationship among Linked Lists


## 5.4.5 Linked List Reading Process

Once configured and enabled by software, the GDMA controller starts to read the linked list from memory. The GDMA performs checks on descriptors in the linked list. Only if descriptors pass the checks, the corresponding GDMA channel will start data transfer. If the descriptors fail any of the checks, hardware will trigger descriptor error interrupt (either AHB_DMA_IN_DSCR_ERR_CHn_INT or AHB_DMA_OUT_DSCR_ERR_CHn_INT), and the channel will halt.

The checks performed on descriptors are:

- Owner bit check when `AHB_DMA_IN_CHECK_OWNER_CHn` or `AHB_DMA_OUT_CHECK_OWNER_CHn` is set to 1. If the owner bit is 0, the buffer is accessed by the CPU. In this case, the owner bit fails the check. The owner bit will not be checked if `AHB_DMA_IN_CHECK_OWNER_CHn` or `AHB_DMA_OUT_CHECK_OWNER_CHn` is 0.

- Descriptor address check, which checks if the descriptor address is located in configured memory space for GDMA. If a GDMA descriptor points to `AHB_DMA_ACCESS_INTR_MEM_START_ADDR ~ AHB_DMA_ACCESS_INTR_MEM_END_ADDR`, it passes the check. For details, please refer to Section 5.4.7.

After the software detects a descriptor error interrupt, it must load new descriptors, and enable GDMA by setting `AHB_DMA_OUTLINK_START_CHn` or `AHB_DMA_INLINK_START_CHn` bit.


## 5.4.6 EOF

**Note:** In this chapter, EOF of transmit descriptors refers to suc_eof (i.e., bit 30 of DWO), while EOF of receive descriptors refers to both suc_eof and err_eof (i.e., bit 28 of DWO).

The GDMA controller uses EOF (end of frame) flags to indicate the end of data segment transfer corresponding to a specific descriptor.

For data transmission, the GDMA generates two types of EOF interrupts:

- `AHB_DMA_OUT_EOF_CHn_INT`, generated when the suc_eof bit of any descriptor in the linked list is set, and the data corresponding to this descriptor has been transmitted. This interrupt is enabled by setting the `AHB_DMA_OUT_EOF_CHn_INT_ENA` bit.
```