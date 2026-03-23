

```markdown
Chapter 34 SDIO Slave Controller (SDIO)

The TX linked list descriptor and the RX linked list descriptor have the same structure, which is shown in Figure 34.5-5. The descriptor consists of 3 words. The meaning of each field is as follows:

*   owner (DW0) [31]: Indicates who is allowed to access the buffer that this descriptor points to.
    0: CPU
    1: DMA engine

    Slave software should set this field to 1 when creating the descriptor. After the DMA write-back permission is enabled and the corresponding buffer is used by the DMA, the field is cleared to 0.

*   eof (DW0) [30]: Indicates the end of a data packet.
    0: The current descriptor is not the last descriptor of the packet
    1: The current descriptor is the last descriptor of the packet

    When the host sends a packet to the slave, the slave software should set the field to 0 while creating the descriptor. DMA sets the field of the last descriptor in the packet to 1; When the host receives packets from the slave, the slave software configures the field depending on whether this descriptor is the last descriptor of the packet.

*   reserved (DW0) [29:28]: reserved.
    Slave software should set this field to 0x0.

*   length (DW0) [27:14]: Indicates the number of valid bytes in the corresponding buffer. When the DMA engine is reading data from the buffer, it indicates the number of bytes that can be read; when DMA engine is storing data in the buffer, it indicates the number of bytes of the stored data.
    When the host sends a packet to the slave, the slave software should set this field to 0x0 while creating the descriptor. DMA writes back the field after the corresponding buffer is used up; when the host receives the packet from the slave and the slave creates the descriptor, the slave software should set this field to the number of bytes that can be read by the corresponding buffer.

*   size (DW0) [13:0]: Indicates the size of the corresponding buffer. Unit: byte.
    Slave software should configure this field when creating the descriptor.
    Note: This field must be word-aligned.

*   buffer address pointer (DW1): Buffer address pointer.
    Slave software should configure this field when creating the descriptor.
    Note: This field must be word-aligned.

*   next descriptor address (DW2): Address of the next descriptor. When the next descriptor does not exist, the value is 0.
    Slave software should configure this field when creating the descriptor.

For more information on DMA write-back linked list descriptor fields, please refer to Section 34.5.5.2.

The slave software can combine multiple descriptors into a linked list using the next descriptor address (DW2) field. The SDIO slave DMA linked list is shown in Figure 34.5-6.
```