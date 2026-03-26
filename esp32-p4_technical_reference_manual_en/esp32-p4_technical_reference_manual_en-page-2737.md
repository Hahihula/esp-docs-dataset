

```markdown
| Bits | Name                     | Description                                                                                                                                                                                                 |
|------|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 30   | CES (Card Error Summary) | This bit indicates the status of the card's read/write operations. This bit is the logical OR of the following bits in the SDHOST_RINTSTS_REG register.<br/>• EBE: End Bit Error<br/>• RTO: Response Timeout<br/>• RCRC: Response CRC<br/>• SBE: Start Bit Error<br/>• DRTO: Data Read Timeout<br/>• DCRC: Data CRC for Receive<br/>• RE: Response Error |
| 29:6 | Reserved                 |                                                                                                                                                                                                             |
| 5    | ER (End of Ring)         | When set to 1, this bit indicates that the linked list has reached its final descriptor. The DMA Controller then returns to the base address of the linked list, creating a linked list ring.                                                                                   |
| 4    | CH (Second Address Chained) | When set to 1, this bit indicates that the second address in the descriptor is the next descriptor address. When this bit is set to 1, BS2 (DES1[25:13]) must be all zeros.                                                                                                     |
| 3    | FD (First Descriptor)    | When set to 1, this bit indicates that this descriptor contains the first buffer of the data. If the size of the first buffer is 0, the next descriptor contains the beginning of the data.                                                                                     |
| 2    | LD (Last Descriptor)     | This bit is associated with the last data block of a DMA transfer. When set to 1, the bit indicates that the buffers pointed by this descriptor are the last buffers of the data. After this descriptor is completed, the remaining byte count is 0. In other words, after the descriptor with the LD bit set is completed, the remaining byte count should be 0. |
| 1    | DIC (Disable Interrupt on Completion) | When set to 1, this bit prevents the setting of the TI/RI bit of the DMA Status Register (SD-HOST_IDSTS_REG) for the data that ends in the buffer pointed by this descriptor.                                                                                           |
| 0    | Reserved                 |                                                                                                                                                                                                             |

The DES1 field contains the buffer size.

Table 54.8-2. DES1 Descriptor Field
| Bits   | Name     | Description |
|--------|----------|-------------|
| 31:26  | Reserved | Reserved    |
| 25:13  | Reserved | Reserved    |
```