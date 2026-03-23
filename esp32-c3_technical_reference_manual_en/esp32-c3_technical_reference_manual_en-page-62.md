

```markdown
## 2.4.1 Linked List

Figure 2.4-1 shows the structure of a linked list. An outlink and an inlink have the same structure. A linked list is formed by one or more descriptors, and each descriptor consists of three words. Linked lists should be in internal RAM for the GDMA engine to be able to use them. The meaning of each field is as follows:

- **Owner (DWO) [31]**: Specifies who is allowed to access the buffer that this descriptor points to.
  - `1'b0`: CPU can access the buffer;
  - `1'b1`: The GDMA controller can access the buffer.

  When the GDMA controller stops using the buffer, this bit in a receive descriptor is automatically cleared by hardware, and this bit in a transmit descriptor is automatically cleared by hardware only if `GDMA_OUT_AUTO_WRBACK_ChN` is set to 1. Software can disable automatic clearing by hardware by setting `GDMA_OUT_LOOP_TEST_ChN` or `GDMA_IN_LOOP_TEST_ChN` bit. When software loads a linked list, this bit should be set to 1.

  **Note**: `GDMA_OUT` is the prefix of transmit channel registers, and `GDMA_IN` is the prefix of receive channel registers.

- **suc_eof (DWO) [30]**: Specifies whether the `GDMA_IN_SUC_EOF_ChN_INT` or `GDMA_OUT_EOF_ChN_INT` interrupt will be triggered when the data corresponding to this descriptor has been received or transmitted.
  - `1'b0`: No interrupt will be triggered after the current descriptor's successful transfer;
  - `1'b1`: An interrupt will be triggered after the current descriptor's successful transfer.

  For receive descriptors, software needs to clear this bit to 0, and hardware will set it to 1 after receiving data containing the EOF flag.
  
  For transmit descriptors, software needs to set this bit to 1 as needed.
  
  If software configures this bit to 1 in a descriptor, the GDMA will include the EOF flag in the data sent to the corresponding peripheral, indicating to the peripheral that this data segment marks the end of one transfer phase.

- **Reserved (DWO) [29]**: Reserved. Value of this bit does not matter.

- **err_eof (DWO) [28]**: Specifies whether the received data has errors.
  
  This bit is used only when UHClO uses GDMA to receive data. When an error is detected in the received data segment corresponding to a descriptor, this bit in the receive descriptor is set to 1 by hardware.

Figure 2.4-1. Structure of a Linked List
```