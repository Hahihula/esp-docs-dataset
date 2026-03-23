

```markdown
## 34.5.4.3 Transferring Fixed-Address Packets

When the host uses address 0x0 to transmit application data packets (such as Bluetooth packets), the address field and OP Code field in CMD53 should be set to 0.

For example, if the host wants to use CMD53 to transfer (send or receive) three data blocks starting from the fixed address 0x0, then it should:

- Set the Block Mode field in CMD53 to 1, indicating data unit is block
- Set the OP Code field to 0, indicating fixed address mode
- Set the Register Address field to 0x0, indicating the fixed address is 0x0
- Set the Byte/Block Count field to 0x3, indicating 3 data blocks
- Set other fields according to the SDIO Specification

When the packet is transmitted (slave sends to host, or slave receives from host) between the host and the slave through CMD53, the slave will determine whether all the valid data of the current packet has been transmitted so as to pad (when slave sends to host) or discard (when slave receives from host) the invalid data. For more information about data padding and discarding, please refer to Section 34.5.5.3.

## 34.5.5 DMA

The SDIO Slave Controller uses a dedicated DMA to access data residing in RAM. As shown in Figure 34.3-1, RAM is accessed over the AHB. For the RAM space accessible by the Controller, please refer to Chapter 5 System and Memory. To set the RAM address range that can be accessed for one transfer, please configure the *SHAREMEM*_REG fields described in Section 34.8.

DMA has two channels, SLCO and SLC1. They are used to transfer incremental-address packets and fixed-address packets, respectively. For the convenience of users, the SDIO slave provides function 1/2 for data transmission. The address range of I/O Function 1/2 is detailed in Section 34.5.4. It is recommended to transmit incremental-address packets via SLCO using function 1 and fixed-address packets via SLC1 using function 2.

DMA accesses RAM over AHB. Users can configure whether the AHB interface can use burst operation and which burst operation type to use by configuring the relevant fields in SDIO_SLCONFO_REG and SDIO_SLC_BURST_LEN_REG. For more information, please refer to Section 34.8.

### 34.5.5.1 Linked List

The slave software can use the DMA engine by mounting linked lists. DMA sends the data from the RAM address space configured in the RX (slave to host) linked list and stores the received data into the address space configured in the TX (host to slave) linked list. A linked list consists of several descriptors.

| 31 | 30 | 29 | 27 | 13 | 0 |
|----|----|----|----|----|---|
| DW0 | owner | eof | reserved | length | size |
| DW1 | buffer address pointer |
| DW2 | next descriptor address |

**Figure 34.5-5. DMA Linked List Descriptor Structure of the SDIO Slave**
```