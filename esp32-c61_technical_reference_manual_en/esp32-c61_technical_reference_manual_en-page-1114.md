

```markdown
5. After the host received the interrupt, it reads from SLCHOST_SLCOHOST_INT_ST_REG, SLCHOST_SLC1HOST_INT_ST_REG, and SLCHOST_PKT_LEN_REG for the following information:

*   SLCHOST_SLC0/1HOST_INT_ST_REG: Interrupt status register. The SLCHOST_SLC0/1_RX_NEW_PACKET_INT_ST bit set to 1 indicates that cause of the interrupt is the slave sending packets.
*   SLCHOST_PKT_LEN_REG: Packet length accumulator register. The current value minus the value of last time equals the packet length sent this time.

6. The host clears the interrupt by writing to the register SLCHOST_SLC0/1HOST_INT_CLR_REG after the CMD52 command.

7. The host fetches packets from the slave after the CMD53 command. During transmission, when the slave determines that the valid data of the current packet is complete, the remaining bits are padded with invalid data (0x0). For details on determining the end of valid data, see Section 30.5.5.3.

8. After the packets are transmitted, the slave DMA sends an interrupt to the CPU, and the CPU can recycle the buffer.

Notes:

*   Do not set all eof bits to 1 in the linked list. Otherwise, the DMA may mistakenly send the next packet’s data as part of the current command, causing errors. If all eof bits are set to 0, the slave software should align the length of each packet to the data block size by padding data, to prevent errors. When the host sends CMD53 to read data, it should accurately control the number of data blocks in each packet and be able to identify the padded data.
*   It is recommended that each CMD53 command transmit only one data packet and each data packet use only one linked list to avoid exceptions caused by complex transmission.
*   Avoid sending multiple packets through one linked list, as it complicates the host and software’s ability to distinguish between packets. If necessary, set the eof bit when creating the linked list to split the packets, so the DMA can pad data accordingly. The length of each packet should be aligned to the data block size to avoid data padding by DMA, and the host should be able to identify the padded data.

30.7.2 Receiving Packets from SDIO Host

Transmission of packets from the host to slave is initiated by the host. The slave receives data via DMA and stores it in RAM. After transmission is complete, the CPU is interrupted to process the data. The procedure is shown in Figure 30.7-2.
```