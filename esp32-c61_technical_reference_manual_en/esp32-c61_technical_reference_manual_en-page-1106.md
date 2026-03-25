

```markdown
## 30.5.4.2 Transferring Incremental-Address Packets

When the host uses addresses 0x400 to 0x1F7FF to transmit multiple application data packets (such as Wi-Fi packets), the address field in CMD53 should be set to increment mode, and the OP Code field should be set to 1.

For example, to transfer (send or receive) three data blocks starting from base address 0x500 using CMD53, the host should:

*   Set the Block Mode field in CMD53 to 1 (block data unit)
*   Set the OP Code field to 1 (incremental address mode)
*   Set the Register Address field to 0x500 (base address)
*   Set the Byte/Block Count field to 0x3 (three data blocks)
*   Set other fields according to the SDIO Specification

When a packet is transmitted (slave to host or host to slave) through CMD53, the slave determines whether all valid data of the current packet has been transmitted and pads (when sending) or discards (when receiving) invalid data as needed. For more information, see Section 30.5.5.3.

## 30.5.4.3 Transferring Fixed-Address Packets

When the host uses address 0x0 to transmit application data packets (such as Bluetooth packets), both the address field and OP Code field in CMD53 should be set to 0.

For example, to transfer (send or receive) three data blocks starting from fixed address 0x0 using CMD53, the host should:

*   Set the Block Mode field in CMD53 to 1 (block data unit)
*   Set the OP Code field to 0 (fixed address mode)
*   Set the Register Address field to 0x0 (fixed address)
*   Set the Byte/Block Count field to 0x3 (three data blocks)
*   Set other fields according to the SDIO Specification

When a packet is transmitted between the host and slave through CMD53, the slave determines whether all valid data of the current packet has been transmitted and pads or discards invalid data as needed. For more information, see Section 30.5.5.3.

## 30.5.5 DMA

The SDIO Slave Controller uses a dedicated DMA to access transfer data from RAM or store it to RAM. As shown in Figure 30.3-1, RAM is accessed over the AHB. For the RAM space accessible by the Controller, please refer to Chapter 4 System and Memory. To set the RAM address range that can be accessed for one transfer, please configure the *SHAREMEM*_REG fields of SLC register described in Section 30.8.

The DMA engine provides two channels: SLCO and SLC1. SLCO is used for transferring incremental-address packets, while SLC1 handles fixed-address packets. The SDIO slave supports two I/O functions (Function 1 and Function 2) for data transmission. It is recommended to use Function 1 with SLCO for incremental-address
```