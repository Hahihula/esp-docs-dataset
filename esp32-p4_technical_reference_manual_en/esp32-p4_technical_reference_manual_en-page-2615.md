

```markdown
| Bits | Name                  | Description                                                                 |
| :---- | :--------------------- | :--------------------------------------------------------------------------- |
| [31:0] | Buffer 1 Address Pointer | These bits indicate the physical address of Buffer 1.                        |

Table 52.4-10. Receive Descriptor 3 (RDES3)
| Bits | Name                  | Description                                                                 |
| :---- | :--------------------- | :--------------------------------------------------------------------------- |
| [31:0] | Buffer 2 Address Pointer<br>(Next Descriptor Address) | These bits indicate the physical address of Buffer 2 when descriptor chaining is used. If the Second Address Chained (RDES1[14]) bit is set, then this address contains the pointer to the physical memory where the Next Descriptor is present. |

Table 52.4-11. Receive Descriptor 4 (RDES4)
| Bits | Name                  | Description                                                                 |
| :---- | :--------------------- | :--------------------------------------------------------------------------- |
| [31:28] | Reserved              | Reserved.                                                                   |
| [27:26] | Reserved              | Reserved.                                                                   |
| [25]   | Reserved              | Reserved.                                                                   |
| [24]   | Reserved              | Reserved.                                                                   |
| [23:21] | Reserved              | Reserved.                                                                   |
| [20:18] | Reserved              | Reserved.                                                                   |
| [17]   | Reserved              | Reserved.                                                                   |
| [16]   | Reserved              | Reserved.                                                                   |
| [15]   | Reserved              | Reserved.                                                                   |
| [14]   | Timestamp Dropped     | When set, this bit indicates that the timestamp was captured for the receive frame but got dropped in the MTL RX FIFO because of overflow. |
| [13]   | PTP Version            | When set, this bit indicates that the received PTP message is having the IEEE 1588 version 2 format. When reset, it has the version 1 format. |
| [12]   | PTP Frame Type         | When set, this bit indicates that the PTP message over Ethernet is sent directly over Ethernet. When this bit is not set and the MT (message type) is not 0, it indicates that the PTP message over UDP-IPv4 or UDP-IPv6 is received. |
```