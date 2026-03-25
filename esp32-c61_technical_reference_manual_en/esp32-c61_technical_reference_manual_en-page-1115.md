

```markdown
Chapter 30 SDIO Slave Controller (SDIO)
GoBack

Figure 30.7-2. Procedure of Slave Receiving Packets from Host

The host obtains the number of available receiving buffers from the slave by accessing SLCHOST_SLCOHOST_TOKEN_RDATA_REG or SLCHOST_SLC1HOST_TOKEN_RDATA_REG. The slave CPU should update the value of the register after the receiving DMA linked list is prepared.

SLCHOST_HOSTSLCHOST_SLC0_TOKEN1 or SLCHOST_HOSTSLCHOST_SLC1_TOKEN1 stores the accumulated number of available buffers. The host can determine the available buffer space by subtracting the number of buffers already used from the register value. If buffers are insufficient, the host should poll the register until enough buffers are available.

During packet transmission to the slave through the CMD53 command, when a buffer specified by a linked list descriptor is full or a packet transmission ends, the DMA jumps to the next buffer to store subsequent data. When the slave determines that the valid data of the current packet is complete, the remaining data is considered invalid and discarded. The DMA writes back the current linked list descriptor, sets the eof bit of the current descriptor to 1, and generates the SLC0/1_TX_SUC_EOF_INT interrupt.

For more information about DMA functions, linked list, and data discarding, see Section 30.5.5.

To ensure sufficient receiving buffers, the slave CPU must continuously load buffers onto the receiving linked list. The process is shown in Figure 30.7-3.
```