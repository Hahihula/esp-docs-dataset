
```markdown
packets and Function 2 with SLC1 for fixed-address packets. For details on the address ranges of these functions, see Section 30.5.4.

DMA accesses RAM over AHB. You can configure the burst operation mode and type by setting the relevant fields of SDIO_SLCCONFO_REG and SDIO_SLC_BURST_LEN_REG. For more information, see Section 30.8.

30.5.5.1 Linked List

The slave software can use the DMA engine by mounting linked lists. The DMA engine transfers data from the RAM address space specified in the RX (slave-to-host) linked list and stores received data in the RAM address space specified in the TX (host-to-slave) linked list. A linked list is composed of multiple descriptors.

| DW0 | owner | eof | reserved | length | size |
|-----|-------|-----|----------|--------|------|
|     |       |     |          |        |      |
| DW1 | buffer address pointer |     |          |        |      |
|     | next descriptor address |     |          |        |      |
| DW2 |       |     |          |        |      |

Figure 30.5-5. DMA Linked List Descriptor Structure of the SDIO Slave

The TX and RX linked list descriptors share the same structure, as shown in Figure 30.5-5. Each descriptor consists of three words, with the following fields:

*   **owner (DW0) [31]:** Specifies the entity allowed to access the buffer.
    0: CPU
    1: DMA engine
    The slave software sets this field to 1 when creating the descriptor. After the DMA write-back permission is enabled and the corresponding buffer is used by the DMA, the field is cleared to 0.

*   **eof (DW0) [30]:** Indicates the end of a data packet.
    0: The current descriptor is not the last descriptor of the packet
    1: The current descriptor is the last descriptor of the packet
    When the host sends a packet to the slave, the slave software should set the field to 0 while creating the descriptor. DMA sets the field of the last descriptor in the packet to 1; When the host receives packets from the slave, the slave software configures the field depending on whether this descriptor is the last descriptor of the packet.

*   **reserved (DW0) [29:28]:** Reserved field.
    The slave software sets this field to 0x0.

*   **length (DW0) [27:14]:** Indicates the number of valid bytes in the corresponding buffer. When the DMA engine is reading data from the buffer, it indicates the number of bytes that can be read; when DMA engine is storing data in the buffer, it indicates the number of bytes of the stored data.
    When the host sends a packet to the slave, the slave software should set this field to 0x0 while creating the descriptor. DMA writes back the field after the corresponding buffer is used up; when the host receives the packet from the slave and the slave creates the descriptor, the slave software should set this field to the number of bytes that can be read by the corresponding buffer.

*   **size (DW0) [13:0]:** Specifies the size of the buffer in bytes.
```