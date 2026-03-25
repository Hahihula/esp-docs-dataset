
```markdown
30.5.5.2 Write-Back of Linked List

When sending packets from the host to the slave, if the buffer specified by a linked list descriptor is full or a packet transmission ends, the DMA engine jumps to the next descriptor to store subsequent data. Before jumping, the DMA writes back the current descriptor. In DWO, the DMA updates the `eof` and `length` bits to their latest values. The value of the `owner` bit is determined by SDIO_SLC0/1_TX_LOOP_TEST in SDIO_SLCCONFO_REG.

When receiving packets from the slave, if the host reads all data in the buffer specified by a linked list descriptor, the DMA engine jumps to the next descriptor to read subsequent data. Before jumping, the slave software can set SDIO_SLC0/1_RX_AUTO_WRBACK in SDIO_SLCCONFO_REG to 1 so that the DMA writes back the current descriptor. The value to write to the `owner` bit is determined by SDIO_SLC0/1_RX_LOOP_TEST in SDIO_SLCCONFO_REG. Other bits in DWO remain unchanged.

The relevant register fields are described in Section 30.8.

30.5.5.3 Data Padding and Discarding

To transfer data in blocks, both the host and the slave pad the data sent on the SDIO bus into entire blocks. The slave automatically pads data when sending a packet and discards the padded data after receiving packets.

- When the host sends a data packet to the slave through CMD53 and the amount of data reaches the packet length, the SDIO slave considers the valid data of the current packet complete. At this time, the DMA writes back the current linked list descriptor, sets the `eof` bit of the current descriptor to 1, and generates the SLC0/1_TX_SUC_EOF_INT interrupt. After determining that the valid data is complete, the remaining data of the current packet is considered invalid and is not received into the buffer by the DMA. The slave does not restart receiving data into the next buffer until the next CMD53.

  - For incremental-address packets, the slave determines valid data based on the address. Data with an address greater than or equal to 0x1F800 is considered invalid and is discarded. Therefore, the host should set the CMD53 start address field to 0x1F800 – Packet_length (in bytes). The data flow of incremental-address packets on the SDIO bus is shown in Figure 30.5-7.

    Figure 30.5-7. Data Flow of Sending Incremental-address Packets From Host to Slave

  - For fixed-address packets, the slave interprets the first three bytes of the data packet as the packet length. These three bytes are also stored in the buffer specified by the linked list. After the received data length matches the value indicated by these three bytes, any subsequent data is considered invalid and discarded.

- When the host receives data packets (including incremental-address and fixed-address packets) from the slave through a CMD53 command, and the DMA reads the last byte of a buffer where the `eof` bit of
```