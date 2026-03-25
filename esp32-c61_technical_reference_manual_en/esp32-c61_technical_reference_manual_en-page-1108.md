

```markdown
Chapter 30 SDIO Slave Controller (SDIO)    GoBack


This field must be word-aligned. The slave software configures it during descriptor creation.
* buffer address pointer (DW1): Points to the buffer address.
  This field must be word-aligned. The slave software configures it during descriptor creation.
* next descriptor address (DW2): Points to the next descriptor in the linked list.
  If no next descriptor exists, this field is set to 0. The slave software configures it during descriptor creation.


For more information on DMA write-back linked list descriptor fields, see Section 30.5.5.2.

The slave software can combine multiple descriptors into a linked list using the next descriptor address (DW2) field. The SDIO slave DMA linked list is shown in Figure 30.5-6.


Figure 30.5-6. DMA Linked List of the SDIO Slave


The following example demonstrates the use of a linked list and the eof bit. Suppose the slave software creates a linked list with three descriptors:

* Descriptor 0 points to 500 bytes of data, with its eof bit set to 0.
* Descriptor 1 points to 200 bytes of data, with its eof bit set to 1.
* Descriptor 2 points to 200 bytes of data, with its eof bit set to 1.

1. If the first CMD53 command requests 400 bytes, the DMA sends the first 400 bytes from Descriptor 0 to the host.
2. If the second CMD53 command requests 400 bytes, the DMA first sends the remaining 100 bytes from Descriptor 0 to the host, followed by 200 bytes from Descriptor 1. Since the eof bit of Descriptor 1 is set to 1, the DMA considers the valid data for the current CMD53 command complete and pads the remaining 100 bytes with invalid data (0x0).
3. If the third CMD53 command requests 400 bytes, the DMA sends 200 bytes from Descriptor 2 to the host. As the eof bit of Descriptor 2 is set to 1, the DMA considers the valid data for the current CMD53 command complete and pads the remaining 200 bytes with invalid data (0x0).
```