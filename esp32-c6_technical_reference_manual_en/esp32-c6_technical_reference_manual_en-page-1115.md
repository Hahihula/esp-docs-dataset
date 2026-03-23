

```markdown
Figure 34.5-6. DMA Linked List of the SDIO Slave

An example is provided below to facilitate understanding of the linked list and the eof bit. Suppose the slave software creates a linked list that contains 3 descriptors; descriptor 0 points to 500 bytes data and its eof bit is 0; descriptor 1 points to 200 bytes data and its eof bit is 1; descriptor 2 points to 200 bytes data and its eof bit is 1. If the first CMD53 needs to read 400 bytes data, then DMA sends the first 400 bytes data of descriptor 0 to the host. If the second CMD53 needs to read 400 bytes data, firstly DMA sends the remaining 100 bytes data of descriptor 0 to the host. Secondly, it sends 200 bytes data of descriptor 1 to the host. Since the eof bit of descriptor 1 is 1, DMA considers the valid data of the current CMD53 is over. So, lastly DMA sends 100 bytes invalid data 0x0 to the host. If the third CMD53 needs to read 400 bytes data, firstly DMA sends the 200 bytes data of descriptor 2 to the host. Since descriptor 2’s eof bit is 1, DMA considers the valid data of current CMD53 is over. So, DMA sends 200 bytes invalid data 0x0 to the host.

34.5.5.2 Write-Back of Linked List

In the process of sending packets from the host to the slave, when the buffer specified by a linked list descriptor is full, or when a packet transmission ends, the DMA engine needs to jump to the next descriptor to store subsequent data. Before the jump, DMA writes back the current descriptor. In DWO, DMA updates the eof and length bits to the latest value. The value of the owner bit is determined by SDIO_SLCO/1_TX_LOOP_TEST in SDIO_SLCCONFO_REG.

In the process of receiving packets from the slave, when the host reads all the data in the buffer specified by a linked list descriptor, DMA engine needs to jump to the next descriptor to read subsequent data. Before the jump, the slave software can set SDIO_SLCO/1_RX_AUTO_WRBACK in SDIO_SLCCONFO_REG to 1 so that the DMA will write back the current descriptor. The value to write to the owner bit is determined by SDIO_SLCO/1_RX_LOOP_TEST in SDIO_SLCCONFO_REG. Values of other bits in DWO remain unchanged.

The relevant register fields are described in Section 34.8.
```