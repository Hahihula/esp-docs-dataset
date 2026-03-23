

```markdown
Chapter 34 SDIO Slave Controller (SDIO)  GoBack


Figure 34.7-2. Procedure of Slave Receiving Packets from Host



The host obtains the number of available receiving buffers from the slave by accessing SLCHOST_SLCOHOST_TOKEN_RDATA_REG or SLCHOST_SLC1HOST_TOKEN_RDATA_REG. The slave CPU should update the value of the register after the receiving DMA linked list is prepared.

SLCHOST_HOSTSLCHOST_SLC0_TOKEN1 or SLCHOST_HOSTSLCHOST_SLC1_TOKEN1 stores the accumulated number of available buffers. The host can figure out the available buffer space, using the register value minus the number of buffers already used. If the buffers are not enough, the host needs to constantly poll the register until there are enough buffers available.

During the transmission of packets to the slave through the CMD53 command, when a buffer specified by a linked list descriptor is written full, or when a packet transmission ends, the DMA will jump to the next buffer to store subsequent data. When the slave determines that the valid data of the current packet is over, the remaining data will be considered invalid and discarded. DMA will write back the current linked list descriptor, set the eof bit of the current descriptor to 1, and the SLCO/1_TX_SUC__EOF_INT interrupt will be generated.

For more information about DMA functions, linked list, and data discarding, please refer to Section 34.5.5.

To ensure sufficient receiving buffers, the slave CPU must constantly load buffers on the receiving linked list. The process is shown in Figure 34.7-3.
```