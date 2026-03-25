

```markdown
Chapter 3 GDMA Controller (GDMA) GoBack

3.4 Functional Description

3.4.1 Linked List

Figure 3.4-1. Structure of a Linked List

Linked List

DW0
DW1
DW2

DW0
DW1
DW2

DW0
DW1
DW2

DW0
DW1
DW2

31   30   29   28   27   23   11    0
DW0 | owner| suc_eof| reserved| err_eof| reserved| length| size
DW1                     buffer address pointer
DW2                    next descriptor address

Figure 3.4-1 shows the structure of a linked list. An outlink and an inlink have the same structure. A linked list is formed by one or more descriptors, and each descriptor consists of three words. Linked lists should be stored in the memory for the GDMA to be able to use them. The meanings of a descriptor's fields are as follows:

• owner (DW0) [31]: Specifies who is allowed to access the buffer that this descriptor points to.
  0: CPU can access the buffer.
    1: The GDMA controller can access the buffer.
      When the GDMA controller stops using the buffer, this bit in a receive descriptor is automatically cleared by hardware, while this bit in a transmit descriptor can only be automatically cleared by hardware if AHB_DMA_OUT_AUTO_WRBACK_CHn is set to 1. Software can disable automatic clearing by hardware by setting the AHB_DMA_OUT_LOOP_TEST_CHn or AHB_DMA_IN_LOOP_TEST_CHn bit. When software loads a linked list, this bit should be set to 1.
      Note: AHB_DMA_OUT is the prefix of transmit channel registers, and AHB_DMA_IN is the prefix of receive channel registers.

• suc_eof (DW0) [30]: Specifies whether the AHB_DMA_IN_SUC_EOF_CHn_INT or AHB_DMA_OUT_EOF_CHn_INT interrupt will be triggered when the data corresponding to this descriptor has been received or transmitted.
  0: No interrupt will be triggered after the current descriptor's successful transfer;
    1: An interrupt will be triggered after the current descriptor's successful transfer.
      For receive descriptors, software needs to clear this bit to 0, and hardware will set it to 1 after receiving data containing the EOF flag.
      For transmit descriptors, software needs to set this bit to 1 as needed.
        If software configures this bit to 1 in a descriptor, the GDMA will include the EOF flag in the data sent to the corresponding peripheral, indicating to the peripheral that this data segment marks the end of one
```